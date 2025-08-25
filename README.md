Step-by-Step Build
Step 1 — Base page setup

What I did: Created the HTML skeleton, set the title, and linked a separate styles.css.
Why this matters: Keeps structure and styles cleanly separated and easier to maintain.

Step 2 — Page heading & helper text

What I did: Added an <h1> and a short <p> above the form.
Why this matters: Gives users context before they start typing.

Step 3 — Form tag with method & action

What I did: Wrapped controls in a <form> with method="post" and action="https://register-demo.freecodecamp.org".
Why this matters: Defines how/where the form submits (useful for testing).

Step 4 — Basic info fieldset

What I did: Added First Name, Last Name, Email, and Password with labels and name attributes.
Why this matters: name is required for values to be sent; using type="email" + required + a password pattern improves validation.

Step 5 — Account type radios

What I did: Added a <fieldset> with a <legend> and two radios sharing name="account-type", plus .inline for neat alignment.
Why this matters: Grouped radios are accessible and ensure only one can be selected.

Step 6 — File upload & age constraints

What I did: Added a file input (profile picture) and a number input for age with min="13" and max="120".
Why this matters: Guides users toward valid input ranges.

Step 7 — Referral select menu

What I did: Created a <select> with a blank default and clear options.
Why this matters: Avoids accidental preselect; makes analytics cleaner.

Step 8 — Bio textarea sizing

What I did: Added rows="3" and cols="30" for an initial size.
Why this matters: Better usability without relying only on CSS.

Step 9 — Terms & conditions (required)

What I did: Added a required checkbox with a TOS link.
Why this matters: Confirms consent before submission.

Step 10 — Submit button

What I did: Added a large, centered submit button with a minimum width for mobile.
Why this matters: Obvious call-to-action improves completion rates.

Step 11 — Styling (CSS)

What I did: Dark theme background, high-contrast text, centered form (60vw, max 500px), full-width inputs, and subtle section dividers.
Why this matters: Readable, accessible, and responsive by default.

Full Code
index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Registration Form</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    <form method="post" action='https://register-demo.freecodecamp.org'>
      <fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" name="first-name" type="text" required /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" name="last-name" type="text" required /></label>
        <label for="email">Enter Your Email: <input id="email" name="email" type="email" required /></label>
        <label for="new-password">Create a New Password: <input id="new-password" name="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
      <fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input id="personal-account" type="radio" name="account-type" class="inline" checked /> Personal</label>
        <label for="business-account"><input id="business-account" type="radio" name="account-type" class="inline" /> Business</label>
      </fieldset>
      <fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" name="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" name="age" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer" name="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
      </fieldset>
      <label for="terms-and-conditions">
        <input class="inline" id="terms-and-conditions" type="checkbox" required name="terms-and-conditions" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
      </label>
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>

styles.css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px;
}

h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
  padding-bottom: 2em;
}

fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}

fieldset:last-of-type {
  border-bottom: none;
}

label {
  display: block;
  margin: 0.5rem 0;
}

input,
textarea,
select {
  margin: 10px 0 0 0;
  width: 100%;
  min-height: 2em;
}

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
}

.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 1em auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
  min-width: 300px;
}

input[type="file"] {
  padding: 1px 2px;
}

a{
  color: #dfdfe2
}


want me to turn this into a printable README.md for your repo (with your preferred bold step titles and the What I did / Why this matters / Before / After sections), or keep it as in-file comments?
