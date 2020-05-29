# LoyJoy JavaScript API

The LoyJoy JavaScript API is a powerful programming interface to control the LoyJoy chat on your website and to personalize the content of your website. The API allows you to show and hide the LoyJoy chat bubble, open and close the chat window, and much more. The events triggered by LoyJoy allow you to react to the chat events, for example using the name entered by the user to address him personally. You can also use LoyJoy as an authentication provider by having your users sign into the chat and then relying on the user data provided by LoyJoy.


## Script integration

The script integration registers the global function LoyJoy in the window. It does not change the DOM. BOT_ID must be replaced with your own ID from the LoyJoy manager.

```
<script src="https://cloud.loyjoy.com/widget/BOT_ID"></script>
```


## Boot

Injects LoyJoy elements into the DOM and shows the chat bubble as configured in the LoyJoy manager.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```


## Events

The chat emits events for chat events (open, close, sign-up, etc.) that can be registered for with event listeners. The registration takes place as catch-all or for specific events.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: [function (evt, obj) {
    // e.g. dataLayer.push({ 'evt': evt, 'bot_id': obj && obj.bot_id, 'process_id': obj && obj.process_id, 'process_name': obj && obj.process_name })
  }],
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: {
    close: [
      function (obj) {}
    ],
    customer: [
      function (obj) {}
    ],
    hide: [
      function (obj) {}
    ],
    load: [
      function (obj) {}
    ],
    open: [
      function (obj) {}
    ],
    participation: [
      function (obj) {}
    ],
    show: [
      function (obj) {}
    ],
    signin: [
      function (obj) {}
    ],
    signout: [
      function (obj) {}
    ],
    signup: [
      function (obj) {}
    ],
    start: [
      function (obj) {}
    ]
  },
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```


## Remove

Removes the LoyJoy DOM elements from the DOM.

```
<script>LoyJoy('remove')</script>
```


## Open

Opens LoyJoy chat. Antagonist to close.

```
<script>LoyJoy('open')</script>
```


## Close

Closes the LoyJoy chat. Antagonist to open.

```
<script>LoyJoy('close')</script>
```


## Hide

Hides the LoyJoy element in DOM (display: none), but does not remove it. Antagonist to show.

```
<script>LoyJoy('hide')</script>
```


## Show

Makes the LoyJoy element visible in DOM. Antagonist to hide.

```
<script>LoyJoy('show')</script>
```


## Cookie consent

A callback function, which signals cookie consent, e.g. from a cookie consent bar on the hosting website.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  cookieConsent: function () {
    return true
    // e.g. return ('; ' + document.cookie).split('; ' + 'MarketingCookiesEnabled' + '=').pop().split(';').shift() == '1'
  },
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```


## Locale

A string in in the format `<language-iso-6391>_<region-iso-31662>` (two-letter-codes). Overwrites the user’s settings regarding language and region. This language and region will be saved as the user’s region and language.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  locale: 'en_US',
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```


## Authentication token

An authentication JSON Web token (JWT), that provides the chat with an authentication context. The JWT issuer is "customer iss" (cf. https://cloud.loyjoy.com/sites/test/jwt.html). The JWT claim "email" is mandatory, the JWT claims "firstname" and "lastname" are optional. The JWT secret is provided in the manager in the tenant settings.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID,
  token: TOKEN
})
</script>
```


## Freely selected parameters

Passes freely selected parameters to the experience that can be evaluated in the BPMN process using BPMN conditions and other expressions.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  params: {
    foo: 'bar'
  },
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```
