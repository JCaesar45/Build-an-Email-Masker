````markdown
# Email Masker

## Overview

This project contains a function that masks the username part of an email address by replacing all but the first and last characters with asterisks (`*`). The domain part remains unchanged.

**Example:**

- Input: `apple.pie@example.com`  
- Output: `a*******e@example.com`

---

## How It Works

The `maskEmail` function:

- Takes an email string as input.
- Splits the email into the username and domain parts.
- Masks the username by keeping the first and last characters visible and replacing the middle characters with `*`.
- Returns the masked email with the original domain.

---

## Usage

```javascript
// Define the maskEmail function
function maskEmail(email) {
  const atIndex = email.indexOf('@');
  const username = email.slice(0, atIndex);
  const domain = email.slice(atIndex);
  const maskedUsername = username[0] + '*'.repeat(username.length - 2) + username[username.length - 1];
  return maskedUsername + domain;
}

// Example usage
const email = "apple.pie@example.com";
console.log(maskEmail(email)); // Output: a*******e@example.com
```

---

## Test Cases

```js
console.log(maskEmail("apple.pie@example.com"));    // a*******e@example.com
console.log(maskEmail("freecodecamp@example.com")); // f**********p@example.com
``

---

## License

This project is open source and available under the MIT License.

```
