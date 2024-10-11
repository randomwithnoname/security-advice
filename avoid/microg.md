# [microG](https://github.com/randomwithnoname/security-advice/tree/main/avoid/microg.md)
microG runs closed source Google Play code with a much weaker app sandbox and permission model compared to regular apps. Each app you install which depends on Google Play contains the Google Play SDK and libraries.

microG itself downloads and runs Google Play code for several of the features it reimplements. That code runs within the privileged microG context and has substantially more access than it does within standard app sandbox. [Sandboxed Google Play](https://grapheneos.org/features#sandboxed-google-play) uses same sandbox as apps using it
