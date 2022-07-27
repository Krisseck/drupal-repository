# Drupal Composer repository

This is [composer](https://getcomposer.org/) repository to include custom Drupal modules/themes.

To use this, your `composer.json` should contain:

```json
"repositories": [
    {
        "type": "composer",
        "url": "https://repository.drupal.hel.ninja/"
    },
]
```

## Adding your own package here

See [Contact](#contact).

## Webhook to automatically update your package

Go to Settings -> Webhooks -> Add webhook

- Payload URL: `https://webhook.drupal.hel.ninja/hooks/update-index`
- Content type: `application/json`

Secret can be found on [Composer repository](https://helsinkisolutionoffice.atlassian.net/wiki/spaces/HEL/pages/6501891919/Composer+repository) confluence page or by contacting us directly. See [Contact](#contact).

## Development

*NOTE:* This is only required on the remote server.

Create .env file that contains:

```
GITHUB_OAUTH=your-github-oauth-token
# This is used to update individual packages
WEBHOOK_SECRET=your-webhook-secret
# This is used by this repository to trigger rebuilds
WEBHOOK_UPDATE_SECRET=your-webhook-secret
```
See [Composer repository](https://helsinkisolutionoffice.atlassian.net/wiki/spaces/HEL/pages/6501891919/Composer+repository) page on confluence for more information.

## Contact

Slack: #helfi-drupal (http://helsinkicity.slack.com/)

Mail: helfi-drupal-aaaactuootjhcono73gc34rj2u@druid.slack.com
