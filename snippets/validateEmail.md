---
title: validateEmail
tags: regex,intermediate
---

Check if the given value is a valid email address.

- Use a regular expression that accepts [RFC 5322](https://www.ietf.org/rfc/rfc5322.txt)
- Convert input string to lowercase
- Use RegExp `test()` method to see if the string is valid email

```js
const validateEmail = email => {
  const regex = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
  return regex.test(String(email).toLowerCase());
}
  
```

```js
validateEmail('helloWorld'); // 'false'
validateEmail('helloWorld@test.com'); // 'true'
```
