# 🐶 DataDog Events - GitHub Action

A GitHub Action that triggers DataDog Events.

## Credit

Heavily based on [jordan-simonovski/datadog-event-action](https://github.com/jordan-simonovski/datadog-event-action) :heart:

## Usage

```
- name: DataDog Event
  uses: Glennmen/datadog-event-action@1.1.0
  with:
    datadog_api_key: ${{ secrets.DD_API_KEY }}
    event_title: Build Succeeded
    event_text: We did it! 🎉
    event_priority: (Can be one of normal or low. Default: normal)
    event_tags: (optional)
    event_alert_type: (Can be one of error, warning, info, or success. Default: info)
    datadog_us: false
```

### Event Tags

Event Tags should be an array of different key/value pairs.

Example:
```
event_tags: "['app:test','env:production']"
```

### Datadog endpoint

By default this action will send events to the Datadog EU endpoint.
This can be overriden to send events to the Datadog US endpoint.

Example:
```
datadog_us: true
```
