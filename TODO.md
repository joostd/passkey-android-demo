This code was adapted from the Google codelab for Credential Manager:

	https://codelabs.developers.google.com/credential-manager-api-for-android

Find the source here:

	https://github.com/android/identity-samples/tree/credman_codelab/CredentialManager

This is the original RP used:

	https://credential-manager-app-test.glitch.me/home

# Documentation

Some docs on passkey support on Android

- https://developer.android.com/training/sign-in/passkeys
- https://developers.google.com/digital-asset-links
- https://developers.google.com/identity/passkeys/supported-environments
- https://medium.com/androiddevelopers/bringing-seamless-authentication-to-your-apps-using-credential-manager-api-b3f0d09e0093
- https://support.google.com/chrome/answer/13168025?hl=en-gb&ref_topic=7439541

# Changes from the original code

8a5e41b updated package names to match iOS version
f23a2ef change name to Pawskey
13e4c23 change colors to green to distinguish from google demo
b66107e upgrade credentials API to Version 1.0.0-alpha08
7ee267e remove password credential provider

# TO DO

- Collapse Fragments into a single one
- Replace assets with backend server calls
