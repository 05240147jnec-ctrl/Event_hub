## Practical IV

**Q1.** A `ReferenceError`, for example `Uncaught ReferenceError: seatsMessage is not defined`. Scripts run top to bottom, so `main.js` has not defined the function yet when `validate.js` calls it.

**Q2.** `document.write()` after the page has loaded reopens the document and replaces everything, so the page goes blank except for the new text. `innerHTML` only changes the content of one chosen element and leaves the rest of the page untouched, which is why it is safer for updates.

**Q3.** No, the form does not clear. `e.preventDefault()` stopped the browser's default reset action when `confirm()` returned `false`.

**Q4.** `ReferenceError: b is not defined`. This proves that `let` is block-scoped: `b` only exists inside the `{ }` of the `if` block. `typeof null` is `"object"`, which is a historical quirk of JavaScript.

**Q5.** The football card is no longer "Sold out": the grey badge becomes a green "5 seats" badge, the message becomes "Filling fast!", the greyed line-through style (`sold-out-card`) disappears, and a Register button appears. On the register page the option is also enabled.

**Q6.** `seatsMessage(0)` returns `"Sold out"`. `seatsMessage(12)` returns `"Filling fast!"` because 12 is not greater than 20 but is greater than 0.

**Q7.** `e.preventDefault()` inside `validateForm()` stops the browser leaving the page. Without it the form would submit (a POST to `#`), the page would reload, and the red error messages would disappear before the user could read them.

**Q8.** `document.querySelectorAll("nav a")` returns a **NodeList**. Yes, `forEach` works on a NodeList in modern browsers (it does not work on an HTMLCollection).
