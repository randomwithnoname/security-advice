[🔗](./microg.md)

microG runs closed-source Google Play code with a much weaker app sandbox and permission model compared to regular apps. Each app you install that depends on Google Play contains the Google Play SDK and libraries.

microG itself downloads and runs Google Play code for several of the features it reimplements. That code runs within the privileged microG context and has substantially more access than it would within the standard app sandbox.

[Sandboxed Google Play](https://grapheneos.org/features#sandboxed-google-play) uses the same sandbox as the apps using it and achieves much broader app compatibility than microG. Android apps work fine on GrapheneOS, except for those [choosing to block all alternate operating systems](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/), which isn't a technical issue with GrapheneOS that they can fix and also applies to operating systems using microG.
