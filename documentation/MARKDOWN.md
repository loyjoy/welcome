# How to add links to chat messages using Markdown

In LoyJoy you can add links to most text messages with the following Markdown format:

```
This is some link [link text](https://www.example.org) to example.org.
```

For the Web chat, such Markdown links will be transformed to normal HTML links, i.e. HTML anchor tags. In case of other channels such as Facebook and WhatsApp the link automatically will be formatted as needed by the channel.


## Trigger events with links instead of following links

Most Web browsers will open a new tab, when the customer clicks on a link generated with the format `[link text](https://www.example.org)`. Thus, this format is best for sending the customer out of the chat to a separate Web browser tab, e.g. for jumping to a separate Web page with terms and conditions.

However, if you want to trigger some JavaScript written by you on a Web page hosting the LoyJoy Web chat, you can use the following format:

```
This is some link [link text](https://www.example.org)(@test) that triggers an event named test.
```

You can choose any event name you like, `test` is just an example. Links formatted this way will trigger an event listener as described in the [LoyJoy JavaScript API](JAVASCRIPT_API.md), which then can call arbitrary JavaScript code written by you:

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: [function (evt, obj) {}],
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```
