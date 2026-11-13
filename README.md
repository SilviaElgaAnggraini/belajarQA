# End-to-End UI Automation Practice (Cypress)

A foundational UI automation testing exercise built with **Cypress** and **JavaScript** to practice automating end-to-end user flows on the [SauceDemo](https://www.saucedemo.com/) web application.

## Project Overview
This repository documents my hands-on learning in basic browser automation, focusing on element selection, user interaction simulation, and assertion handling for a standard e-commerce happy path.

## Test Scenario Covered
**File:** `cypress/e2e/login_dan_checkout.cy.js`

The automated script validates the complete end-to-end purchase flow:
1. **Authentication:** Navigates to `saucedemo.com` and logs in using valid dummy credentials (`standard_user`).
2. **URL Verification:** Confirms successful redirection to the product catalog page (`/inventory.html`).
3. **Cart Management:** Adds the *Sauce Labs Backpack* item to the shopping cart and opens the cart page.
4. **Checkout Flow:** Proceeds to checkout, fills in customer shipping details (`First Name`, `Last Name`, `Postal Code`), and completes the order.
5. **Order Confirmation:** Asserts that the confirmation banner displays `"Thank you"`.

## Tech Stack
* **Framework:** Cypress
* **Language:** JavaScript
* **Target Application:** SauceDemo (`https://www.saucedemo.com/`)

## Project Structure
```text
├── cypress/
│   ├── e2e/
│   │   └── login_dan_checkout.cy.js   # Main E2E test specification
│   ├── fixtures/
│   │   └── example.json               # Static test data
│   └── support/
│       ├── commands.js                # Custom Cypress commands
│       └── e2e.js                     # Global configuration and behavior
├── cypress.config.js                  # Cypress configuration file
└── package.json                       # Project dependencies and scripts
