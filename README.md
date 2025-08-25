Registration Form

A clean, accessible registration form built with semantic HTML and responsive CSS. It includes required fields, validation, grouped radios, a file upload, select menu, textarea sizing, and a required TOS checkbox — all styled with a dark theme.

How to Run

Create two files in the same folder: index.html and styles.css.

Paste the code from the Full Code section below.

Open index.html in your browser.

Steps
Step 1 — Base page setup

<u>What I did</u>: Created the HTML skeleton, set the title, and linked a separate styles.css.
<u>Why this matters</u>: Separating structure and style keeps things clean and maintainable.
<u>Before</u>:

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
      <title>Registration Form</title>
  </head>
  <body></body>
</html>


<u>After</u>:

<link rel="stylesheet" href="styles.css" />

Step 2 — Page heading & helper text

<u>What I did</u>: Added an <h1> and a short <p> above the form.
<u>Why this matters</u>: Gives users context before they start typing.
<u>Before</u>:

<body></body>


<u>After</u>:

<h1>Registration Form</h1>
<p>Please fill out this form with the required information</p>

Step 3 — Form tag with method & action

<u>What I did</u>: Wrapped controls in a <form> with method="post" and action="https://register-demo.freecodecamp.org".
<u>Why this matters</u>: Defines how/where the form submits — useful for testing or integrating a backend.
<u>Before</u>:

<form>
  <!-- inputs -->
</form>


<u>After</u>:

<form method="post" action="https://register-demo.freecodecamp.org">
  <!-- inputs -->
</form>

Step 4 — Basic info fieldset

<u>What I did</u>: Added First Name, Last Name, Email, and Password with labels and name attributes. Included required and a password pattern.
<u>Why this matters</u>: name is needed for submission; built-in validation improves UX.
<u>Before</u>:

<input id="first-name" type="text">
<input id="email" type="email">
<input id="new-password" type="password">


<u>After</u>:

<fieldset>
  <label for="first-name">Enter Your First Name:
    <input id="first-name" name="first-name" type="text" required />
  </label>
  <label for="last-name">Enter Your Last Name:
    <input id="last-name" name="last-name" type="text" required />
  </label>
  <label for="email">Enter Your Email:
    <input id="email" name="email" type="email" required />
  </label>
  <label for="new-password">Create a New Password:
    <input id="new-password" name="new-password" type="password" pattern="[a-z0-5]{8,}" required />
  </label>
</fieldset>

Step 5 — Account type radios

<u>What I did</u>: Grouped radios inside a <fieldset> with a <legend>. Used a shared name="account-type" and .inline to keep controls aligned with labels.
<u>Why this matters</u>: Grouping is accessible and ensures only one choice is selected.
<u>Before</u>:

<input id="personal-account" type="radio">
<input id="business-account" type="radio">


<u>After</u>:

<fieldset>
  <legend>Account type (required)</legend>
  <label for="personal-account">
    <input id="personal-account" type="radio" name="account-type" class="inline" checked /> Personal
  </label>
  <label for="business-account">
    <input id="business-account" type="radio" name="account-type" class="inline" /> Business
  </label>
</fieldset>

Step 6 — File upload & age constraints

<u>What I did</u>: Added a file input for profile picture and a number input for age with min="13" and max="120".
<u>Why this matters</u>: Constrains input to valid ranges and clarifies expectations.
<u>Before</u>:

<input id="age" type="number">


<u>After</u>:

<fieldset>
  <label for="profile-picture">Upload a profile picture:
    <input id="profile-picture" type="file" name="file" />
  </label>
  <label for="age">Input your age (years):
    <input id="age" type="number" name="age" min="13" max="120" />
  </label>
</fieldset>

Step 7 — Referral select menu

<u>What I did</u>: Created a <select> with a blank default and clear option values.
<u>Why this matters</u>: Avoids accidental preselection and supports simple analytics.
<u>Before</u>:

<select id="referrer"></select>


<u>After</u>:

<label for="referrer">How did you hear about us?
  <select id="referrer" name="referrer">
    <option value="">(select one)</option>
    <option value="1">freeCodeCamp News</option>
    <option value="2">freeCodeCamp YouTube Channel</option>
    <option value="3">freeCodeCamp Forum</option>
    <option value="4">Other</option>
  </select>
</label>

Step 8 — Bio textarea sizing

<u>What I did</u>: Sized the textarea with rows="3" and cols="30".
<u>Why this matters</u>: Improves usability without relying only on CSS.
<u>Before</u>:

<textarea id="bio" name="bio" placeholder="I like coding on the beach..."></textarea>


<u>After</u>:

<label for="bio">Provide a bio:
  <textarea id="bio" name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
</label>

Step 9 — Terms & conditions (required)

<u>What I did</u>: Added a required checkbox with a link to the TOS.
<u>Why this matters</u>: Ensures users consent before submission.
<u>Before</u>:

<input id="terms-and-conditions" type="checkbox">


<u>After</u>:

<label for="terms-and-conditions">
  <input class="inline" id="terms-and-conditions" type="checkbox" required name="terms-and-conditions" />
  I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
</label>

Step 10 — Submit button

<u>What I did</u>: Added a large, centered submit button with a minimum width for smaller screens.
<u>Why this matters</u>: Clear call-to-action improves completion.
<u>Before</u>:

<!-- none -->


<u>After</u>:

<input type="submit" value="Submit" />

Step 11 — Styling (CSS)

<u>What I did</u>: Dark theme, high contrast text, centered responsive form (60vw, max 500px), full-width inputs, and .inline class for radios/checkboxes.
<u>Why this matters</u>: Better readability, accessibility, and responsiveness.
<u>Before</u>:

/* minimal or no styles */


<u>After</u>:

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

a {
  color: #dfdfe2;
}

Accessibility Notes

Labels wrap inputs to enlarge clickable area.

Radios grouped with a <legend> for screen reader context.

High contrast palette and large touch targets.

Built-in browser validation on required fields.

Files

index.html — Structure and semantics

styles.css — Layout and theming
