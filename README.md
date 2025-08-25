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
