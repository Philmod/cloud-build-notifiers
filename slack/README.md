# Cloud Build Slack Notifier

This notifier uses [Slack Webhooks](https://api.slack.com/messaging/webhooks) to
send notifications to your Slack workspace.

> This is an Alpha release of Cloud Build Notifiers.
> This codebase might be changed in ways that are not backwards-compatible.
> We do not recommend using this codebase for production applications.
> Furthermore, this release is not subject to any SLA or deprecation policy.

This notifier runs as a container via Google Cloud Run and responds to
events that Cloud Build publishes via its
[Pub/Sub topic](https://cloud.google.com/cloud-build/docs/send-build-notifications).

For detailed instructions on setting up this notifier,
see [Configuring Slack notifications](https://cloud.google.com/cloud-build/docs/configure-notifications#configuring_slack_notifications).

## Configuration Variables

This notifier expects the following fields in the `delivery` map to be set:

- `webhook_url`: The `secretRef: <Slack-webhook-URL>` map that references the
Slack webhook URL resource path in the `secrets` section.
