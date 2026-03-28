# KASIUS Website — Purchase Experience Polish

## Previous Work (Complete)
- About page, Use Cases page, Navigation bar, Stripe Pre-Order buttons — all done.

## Current Tasks

### 1. Trust line under pricing grid
- [x] Add CSS for `.trust-line` (small font, muted color, inline SVG lock icon)
- [x] Add trust line HTML below `.pricing-grid`: "Secure checkout powered by Stripe. 256-bit encryption."
- [x] Add confirmation note below pricing subtitle: "After purchase, you'll receive a confirmation email with shipping details and your estimated delivery date."

### 2. Bottom CTA link fix
- [x] Update `#download` "Pre-Order Now" button → 1TB Stripe link with `target="_blank"` and `rel="noopener noreferrer"`

### 3. Audit and fix all `href="#"` placeholder links
- [x] index.html — fixed the only remaining `href="#"` (bottom CTA button, now points to 1TB Stripe link)
- [x] about.html — no `href="#"` links found (clean)
- [x] use-cases.html — no `href="#"` links found (clean)

### 4. Final review
- [x] Verified changes match existing glassmorphism aesthetic
- [x] Updated progress.md with final status summary

---

## Final Status Summary

**All tasks complete.** Here's what was delivered:

- **Trust line** — Added a subtle "Secure checkout powered by Stripe. 256-bit encryption." line with an inline SVG lock icon below the pricing grid. Styled with muted color at 60% opacity, 0.8rem font — subtle and non-intrusive.

- **Confirmation note** — Added "After purchase, you'll receive a confirmation email with shipping details and your estimated delivery date." below the pricing subtitle, styled with muted text at 80% opacity.

- **Bottom CTA button** — The "Pre-Order Now" button in the `#download` section now links to the 1TB Stripe checkout (most popular) with `target="_blank"` and `rel="noopener noreferrer"`.

- **href="#" audit** — Only one placeholder link existed (the bottom CTA button). It has been fixed. `about.html` and `use-cases.html` had no placeholder links.

**Status:** Complete

---

## Email Signup → Google Sheet Integration

### 1. Google Apps Script code & deployment instructions
- [x] Wrote Apps Script with `doPost` (parses email, appends row with Email + Timestamp) and `doGet` (health check)
- [x] Returns JSON responses, handles errors
- [x] Provided step-by-step deployment instructions (Web app, Execute as Me, Anyone can access)
- [x] Reminded to add column headers: A1 = "Email", B1 = "Timestamp"

### 2. Update website signup form handler
- [x] Updated `#signupForm` submit handler in index.html to POST email to Apps Script URL
- [x] Button shows "Sending..." and disables during request
- [x] On success: hides form + `.signup-note`, shows `#signupSuccess`
- [x] On error: shows inline "Something went wrong. Try again." message, re-enables button
- [x] No CSS or layout changes — only JavaScript modified
- [x] Placeholder `YOUR_APPS_SCRIPT_URL` ready for find-and-replace

### 3. Column headers reminder
- [x] Instructions include adding "Email" in A1 and "Timestamp" in B1 before deploying

**Status:** Complete — replace `YOUR_APPS_SCRIPT_URL` in index.html with the deployed Apps Script URL
