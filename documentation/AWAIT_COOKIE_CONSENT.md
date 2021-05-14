# How to await cookie consent before starting LoyJoy

## 1. What this solution will do for you

In some cases you want to use something like a cookie consent popup that
overlaps with e.g. the LoyJoy chat bubble. In such cases one solution can be to
only start LoyJoy once cookie consent has been handled.

This solution will show you how such a delayed start of LoyJoy can be implemented.

## 2. What you need for this solution to work

You will need to adjust the integration JavaScript snippet and you will need to
determine what changes on your website once cookie consent is handled.

## 3. Determine what changes after cookie consent

One way to do this is to inspect the cookie banner while it is shown. This can
be done in most browsers by right clicking the cookie banner -> `Inspect
element`. To be shown the cookie banner again you can delete your cookies or 
open your website in a private window.

Usually, the cookie banner will have a root element with an ID or class that is
distinct. For example `s-cookie`, or `xy-cookie-policy-popup`.

When you have found the root element, you can accept / decline cookies and
check how the element changes. Often, the cookie banner will simply get a
`display: none` style. In other cases, the whole element might be destroyed
(removed from the DOM).

## 4. Check for cookie banner before starting LoyJoy

Now that you know what to check for regarding the cookie banner, we can
condition starting LoyJoy on whether the banner is still shown or not.

To do this, we define the function `checkAndStart`. This function checks
whether the cookie consent banner is still shown and starts LoyJoy if it
is not. Otherwise it calls itself again, after a wait of 0.4 seconds.

```html
<script src="https://cloud.loyjoy.com/widget/BOT_ID"></script>
<script>
  function checkAndStart() {
    
    const popups = document.getElementsByClassName("s-cookie");
    // get the cookie banner element

    // here you can change the condition
    if (popups.length > 0 && window.getComputedStyle(popups[0]).display === "none") {
      // simply start LoyJoy
      LoyJoy("boot", {
        bot:"<BOT_ID>",
        cookieConsent: function() {
          return "0" == ("; "+document.cookie).split("; MarketingCookiesDisabled\x3d").pop().split(";").shift()
        },
        process:"<PROCESS_ID>"
      });
    } else {
      setTimeout(checkAndStart, 400);
      // check again in 0.4 seconds
    }
  }
  checkAndStart()
  // initialize checking
</script>
```

Now you can simply add the changed snippet to your website, replacing the old snippet. 
