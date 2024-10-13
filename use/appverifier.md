[🔗](https://github.com/randomwithnoname/security-advice/tree/main/use/appverifier.md)

[AppVerifier](https://github.com/soupslurpr/AppVerifier) is not an app store or a way to obtain apps. It's simply an app signing certificate hash viewer and verifier, which can be useful when obtaining apps without using an app store that has robust validity guarantees for installed apps. 

You only need to verify the initial installation, as Android prevents installing updates that aren't signed by the same key or a key authorized by it, as well as versions older than the one currently installed.

AppVerifier includes a pinning database for signing key fingerprints along with manual verification to validate the authenticity by comparing the certificate fingerprint against the fingerprint from another source (it wouldn’t matter otherwise).

[Obtainium](https://github.com/randomwithnoname/security-advice/tree/main/use/obtainium.md) has built-in support for AppVerifier.
