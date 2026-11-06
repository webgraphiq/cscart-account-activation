# Account Activation for CS-Cart

**🛑 PREMIUM ADD-ON: This repository does not contain the open-source code. It serves as the official listing and documentation page for the WebGraphiq premium add-on.**

**Account Activation** is a double opt-in and email-confirmation add-on for CS-Cart and Multi-Vendor. New customers receive an activation link after registration; the account exists, but they cannot sign in until they confirm the email. That keeps fake sign-ups out of the storefront and gives B2B shops a clear identity step before login.

## [🛒 Buy & View Live Demo](https://www.webgraphiq.com/account-verify.html)

One-time license. The current price and the live demo are on the product page.

## Why store owners use it

- Require email verification before the customer can sign in — classic double opt-in for CS-Cart registrations.
- Registration sends an activation email with a one-click link; until then the account stays closed.
- Optionally require confirmation **only when the checkout cart is free** (paid checkouts can skip the gate).
- Automatically remove customer accounts that stay unconfirmed for more than **24 hours**.
- Separate redirects after storefront registration vs checkout registration (CS-Cart dispatch or path you choose).
- On Multi-Vendor, optionally let **vendors** activate their own account without waiting for an administrator.
- Built for CS-Cart / Multi-Vendor **4.12.1+** including **4.21**, PHP **8.3**-ready; current package ships as readable PHP under the WebGraphiq commercial license.

## How activation works

1. The shopper registers (storefront profile or during checkout, depending on your flow).
2. CS-Cart creates the user; Account Activation marks the account as needing confirmation and sends the activation mail.
3. Until the link is opened, sign-in stays blocked; the storefront shows the activation notice instead of a generic “account created” success when confirmation is required.
4. The customer clicks the link (`wg_auth.activation`); the account is confirmed and they are redirected to the path you configured.
5. Administrators can still mark a user Active in the admin — that also counts as confirmed.

Failed registrations (for example a password that is too short) do not send the activation email or show the yellow activation notice. When confirmation is required, the stock “new profile” mail with login details is suppressed so only the activation message goes out.

## What you control

| Setting | Purpose |
|---|---|
| **Only on free products at checkout** | Ask for confirmation when the cart total is free; otherwise follow your broader registration rules. |
| **Remove unconfirmed accounts (24+ hours)** | Cron-style cleanup of stale, never-confirmed customer accounts. |
| **Redirect on registration activation** | Where to send the customer after a successful storefront activation (default `profiles.success_add`). |
| **Redirect on checkout registration activation** | Separate target after confirming from a checkout registration (default `checkout.checkout`). |
| **Allow vendors to activate their account** | Multi-Vendor: vendors confirm themselves when enabled; otherwise admin approval remains. |

## Requirements

- CS-Cart or Multi-Vendor **4.12.1** or newer, including **4.21**
- PHP **8.3** or a current 8.x release used by that shop
- License key from your WebGraphiq order (entered under the add-on settings)

## This repository

<p align="center">
  <a href="https://www.webgraphiq.com/account-verify.html">
    <img alt="Buy and view the live demo" src="https://img.shields.io/badge/CS--Cart-Buy%20%26%20View%20Live%20Demo-28a745?style=for-the-badge&labelColor=1A365D">
  </a>
</p>

<p align="center"><strong>One-time license · email confirmation before sign-in</strong></p>

This is the public product listing. The add-on package, license checks, and source files are not published here. After purchase, the package is readable PHP under the WebGraphiq commercial license, installed from your WebGraphiq account.

Support: [webgraphiq.com](https://www.webgraphiq.com) · webgraphiq@gmail.com

© WebGraphiq. All rights reserved. [License](https://www.webgraphiq.com/license.html)

## Other Premium CS-Cart Add-ons by WebGraphiq

More CS-Cart and Multi-Vendor add-ons are listed on the [WebGraphiq GitHub profile](https://github.com/webgraphiq).
