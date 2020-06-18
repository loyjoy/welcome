# WebService Integration

The WebService process building block enables connecting LoyJoy to external APIs. As soon as the chat flow arrives at an WebService process building block, a synchronous HTTP POST request is sent to the configured URL. 

The request body is structured as follows:

```json
{
  "data": {
    "message": {
      ...
    }
  },
  "params": {
    "referrer": REFERRER,
    "user-agent": USER_AGENT,
    ...
  },
  "variables": {
    "customer_email": CUSTOMER_EMAIL,
    ...
  }
}
```


The WebService endpoint has to respond after a few seconds. It optionally can provide variables to be set in the process instance as well as a chat message as follows:

```json
{
  "variables": {
    "some_key": "some_value",
    ...
  }
}
```

