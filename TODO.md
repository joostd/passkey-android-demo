- codelab:
	https://codelabs.developers.google.com/credential-manager-api-for-android#0

- source:
	https://github.com/android/identity-samples/tree/credman_codelab/CredentialManager

- RP:
	https://credential-manager-app-test.glitch.me/home

https://developers.google.com/digital-asset-links/v1/getting-started
https://developer.android.com/training/sign-in/passkeys
https://developers.google.com/digital-asset-links
https://medium.com/androiddevelopers/bringing-seamless-authentication-to-your-apps-using-credential-manager-api-b3f0d09e0093
https://developers.google.com/identity/passkeys/supported-environments
https://support.google.com/chrome/answer/13168025?hl=en-gb&ref_topic=7439541
https://developers.google.com/identity/passkeys/supported-environments

# TODO

move assetlinks to rp.joostd.nl
https://credential-manager-app-test.glitch.me/.well-known/assetlinks.json

update cert

check commit: https://github.com/android/identity-samples/commit/735c32611ee71e09ee15ad2abdb35088ecda6bcb


```
$ grep = keystore.properties
storePassword=android
keyPassword=android
keyAlias=androiddebugkey
storeFile=../debug.keystore

$ keytool -list -keystore debug.keystore -storepass android -alias androiddebugkey
androiddebugkey, 31 Jan 2023, PrivateKeyEntry, 
Certificate fingerprint (SHA-256): 4F:20:47:1F:D9:9A:BA:96:47:8D:59:27:C2:C8:A6:EA:8E:D2:8D:14:C0:B6:A2:39:99:9F:A3:4D:47:3D:FA:11

$ curl -s https://credential-manager-app-test.glitch.me/.well-known/assetlinks.json | jq '.[].target|select(.namespace=="android_app").sha256_cert_fingerprints[]'
"4F:20:47:1F:D9:9A:BA:96:47:8D:59:27:C2:C8:A6:EA:8E:D2:8D:14:C0:B6:A2:39:99:9F:A3:4D:47:3D:FA:11"
```

