Log-To-Slack Ansible role
==========================

This is an Ansible role for setting up live streaming of log files to a Slack channel using `syslog-ng`.

#### Required variables
```yaml
# Slack API webhook
lts_slack_webhook: https://hooks.slack.com/services/XXXXXX/XXXXXXXX/XXXXXXXXXXXXXXXX

# Path to log file
lts_log_path: /var/log/some-log-file.log
```

#### Basic Customisations
```yaml
# Default "author" field shown in Slack messages
lts_slack_author: log-to-slack

# String or regular expression to match against log lines.
# Only *matching* lines will be sent to Slack. Default matches anything.
# Example: "FATAL ERROR"
lts_syslogng_regex: .
```

#### Advanced Customisations

See variables and notes in `/defaults/main` and `/templates`.

Docs for syslog-ng: https://www.syslog-ng.com/technical-documents/doc/syslog-ng-open-source-edition/3.26/administration-guide

Docs for Slack API: https://api.slack.com/messaging/webhooks
