---
title: "JavaScript GOTCHAs"
excerpt: "Beware of JS traps."
header:
 # overlay_image: /assets/images/2017/android/cover.png
  overlay_color: "#333"
  overlay_filter: 0.5

date: "2019-03-05 06:00:00"
categories: javascript
---

# Date

### Date object constructor waits to break your code

Creation of Date object is tricky. First look at the `new Date(2019, 1, 5)` suggest that the object is represeting 5th of January, 2019 - *WRONG* - year and day are correct but months are counted from `0` so 1st month in this case is February. For January we need to create `new Date(2019, 0, 5)`.

It may cause errors when you are trying to create dates from strings you are receiving. For example your date picker returns `07-09-2019` for seventh of September, 2019 and you want to convert it into Date object. It would be comfy to make variables from the string to get such object: `{day: 7, month: 9, year: 2019}` now to create proper date remember to substract 1 from month and we get `greatParty = new Date(year, month - 1, day)`.

In english version of [Mozilla's documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) we can see `new Date(year, monthIndex, [day…` but on some other languages it just says `new Date(year, month, [day…`. Here this `Index` postfix is crucial - if you see such translation in your native language I encurage you to fix this.

### GetYear from Date object will leave you in uncertainty

JavaScript gives us methods to exctract parts of Date i.e `.getMonth()`, `.getDay()`, `.getYear()`, `getFullYear()` etc. Wait what? Is there a difference between the two year functions? Of course it is! Long story short `getYear()` returns a year minus 1900. For `2019` it will return `119` and for `1989` it will return `89`. Good thing is that `getFullYear()` behaves as expected.

Method `.getYear()` is also marked as deprecated in documentation but by looking on other methods analogy or without well configured linter you may fall into the trap and use it.

