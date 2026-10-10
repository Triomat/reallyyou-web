# Really you? – browser check

Static page for the [Really you?](https://github.com/Triomat/reallyyou) Android app. When someone says their phone is broken, the app sends them a link to this page. They open it on any smartphone, without installing anything, and prove who they are:

- **Key card:** tap a FIDO security key (card, ring, keychain) on the phone. Uses WebAuthn, so it works in Chrome on Android and Safari on iPhone.
- **Photo check:** pick the one photo they recognize among 9, three rounds in a row.

The page talks to the app through [ntfy](https://ntfy.sh) on a one-time topic derived from the secret in the link. The secret stays in the URL fragment and is never sent to GitHub. Photos are encrypted end to end with a key derived from the same secret.

Served by GitHub Pages at https://triomat.github.io/reallyyou-web/. Key cards are registered by the app for the domain `triomat.github.io`, so this page must stay on that domain.
