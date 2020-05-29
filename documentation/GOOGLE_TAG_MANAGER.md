# Integrate data from your LoyJoy chat into your tracking solution

With a LoyJoy chat on your site you can connect with your customers in a great way. You can watch how your customers use the chat in the LoyJoy backend. You can also extract a lot of data from LoyJoy and integrate it directly into your own website tracking solution to collect all analytics data in one place.

## Tracking integration

The tracking integration is based on the LoyJoy JavaScript API. Through the JavaScript API, events are triggered for various events in the chat:


| Event name          | Event description |
|---------------------|------------------|
| hide                | The chat window was not displayed when loading or hidden (hidden) after loading via JavaScript API. |
| load                | The chat was loaded. |
| open                | The chat was opened. |
| show                | The chat was displayed / no longer hidden. |
| start               | A first message was sent in the chat (if no preview messages are set this means that the chat was opened). |
| participation       | A customer has taken part in a competition in the chat. |
| signin              | A customer has logged in to the chat. |
| close               | The chat was closed by the customer or via API. |
| signup              | A customer has registered in the chat. |
| customer            | A customer entered new data (also contains data). |
| signout             | A customer has logged out of the chat. |
| newsletter_opt_in   | A customer accepted a newsletter in chat (single opt-in). |
| profiling_opt_in    | A customer has accepted profiling in chat (single opt-in). |
| reminder_opt_in     | A customer has accepted a reminder in chat (single opt-in). |


Using the following code to integrate a LoyJoy chat in your site, LoyJoy events can be pushed to an existing Google Tag Manager data layer:

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: [function (evt, obj) {
    dataLayer && dataLayer.push({ 'event': 'loyjoy', 'gaEventCategory': 'loyjoy', 'gaEventAction': obj && obj.process_name, 'gaEventLabel': evt })
  }],
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```

