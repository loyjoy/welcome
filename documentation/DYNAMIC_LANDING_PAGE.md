# How to conduct A/B testing in LoyJoy

## 1. What this solution will do for your

This article is right for you if you want run an A/B test with two (or more) different chats on the same website.

## 2. What you need for this solution to work

This article offers three different options for A/B testing. The first two options require to modify JavaScript on your website. The third options works by just adding a parameter to the URL.

## 3. There are three options for A/B testing

There are three ways to have dynamic experiences on one landing page:
- Switching experiences in the website's JavaScript
- Switching experiences in LoyJoy based on parameters from the website's JavaScript
- Switching experiences based on freely defined URL parameters

## 4. First option: switching experiences in JavaScript

You can `boot` LoyJoy with different processes, depending on conditions you choose. 

One common condition is a URL parameter. See this example:

```javascript
const loyjoyParam = getParameterByName("loyjoy-process");

let process;

if (loyjoyParam == null) {
  process = "<default-process-id>"; // default: Navigation über Landing Page
} else if (loyjoyParam === "quiz") {
  process = "<quiz-process-id>"; // Quizzes
}

LoyJoy("boot", {
  "bot": "<bot-id>",
  "process": process
})
```

Here, `loyjoy-process` is the URL parameter we chose to determine which process to `boot`. `getParameterByName` is
simply a function that gets us the value of URL paramter.

## 5. Second option: switching Experiences in LoyJoy

When booting LoyJoy, we can hand over arbitrary parameters:

```javascript
LoyJoy("boot", {
  "bot": "<bot-id>",
  "params": {
    "myparam": user.hasCamera
  },
  "process": "<process-id>"
})
```

The parameter `myparam` is now freely available in LoyJoy. Parameter names can be chosen freely.

Inside LoyJoy, we can access this parameter and, for example, make an automatic jump based on it:

![condition](dynamic_landing_page/process-jump-condition.png)

Here, we trigger an automatic jump, if the given parameter is has the value `true`. This jump can lead
to a specific position in the process or to another process altogether.

## 6. Third option: switching experiences with URL parameters

Let's say your website has the URL `https://www.example.org`. Just use two or more parameters that you can access in LoyJoy like this:

`https://www.example.org?loyjoy-myparam=value1`

and

`https://www.example.org?loyjoy-myparam=value2`

Inside LoyJoy, we can access this parameter and, for example, make an automatic jump based on it:

![condition](dynamic_landing_page/process-jump-condition.png)

Here, we trigger an automatic jump, if the given parameter is has the value `true`. This jump can lead
to a specific position in the process or to another process altogether.

