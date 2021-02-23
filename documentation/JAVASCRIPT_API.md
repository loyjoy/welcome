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

The chat emits events for chat events (open, close, sign-up, etc.) that can be registered for with event listeners. The registration takes place either as a catch-all ...

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

... or for specific events:

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  eventListeners: {
    close: [
      function (obj) {}
    ],
    customer_created: [
      function (obj) {}
    ],
    hide: [
      function (obj) {}
    ],
    interaction: [
      function (obj) {}
    ],
    load: [
      function (obj) {}
    ],
    open: [
      function (obj) {}
    ],
    show: [
      function (obj) {}
    ],
    sign_in: [
      function (obj) {}
    ],
    sign_out: [
      function (obj) {}
    ],
    sign_up: [
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

### Event Token

Events can include a `token` field. This token is a JSON web token with the issuer `map iss` and includes the email, as well as optionally the first name and last name of logged-in users. One example for such a token with the secret `test-secret`:

```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJtYXAgaXNzIiwiZW1haWwiOiJ0ZXN0QGxveWpveS5jb20ifQ.CjH4UxbVkCLfZ19Tz7_9_gjRCaFf6fkYbuUtnDPFmOw
```

The secret for this token can be set in the tenant settings in the tenant tab in the field `Secret JWT key`.

A full event object looks like this:

```JSON
{
  "bot_id": "79afa326-74d3-44ac-a645-da5554fa685c",
  "process_id": "ef613f3d-1390-4796-8c95-58a19f44e14f",
  "process_name": "Test-Name",
  "email": "test@loyjoy.com",
  "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJtYXAgaXNzIiwiZW1haWwiOiJ0ZXN0QGxveWpveS5jb20ifQ.CjH4UxbVkCLfZ19Tz7_9_gjRCaFf6fkYbuUtnDPFmOw"
}
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

A string in in the format `<language-iso-6391>_<region-iso-31662>` (two-letter-codes). Overwrites the user’s settings regarding language and region. This language and region will be saved as the user’s language and region.

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

## Restart

Tells the chat to restart the process after after a page reload (or after a new `LoyJoy('boot')`).

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  restart: true,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```

## Open

Tells the chat to open the messenger window independent of other configuration settings.

```
<script>
LoyJoy('boot', {
  bot: BOT_ID,
  open: true,
  process: OPTIONAL_PROCESS_ID,
  serviceWorkerPath: OPTIONAL_SERVICE_WORKER_PATH,
  tenant: OPTIONAL_TENANT_ID
})
</script>
```
