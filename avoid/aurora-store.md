# [Aurora Store](https://github.com/randomwithnoname/security-advice/tree/main/avoid/aurora-store.md)
Aurora Store simply downloads apps from the Play Store including the Google Play SDK and libraries included in many of the apps. Most of the APKs are generated and signed by Google Play. You aren't avoiding Google Play or hiding the details of your device from them with it.

Aurora Store does not verify the signatures of apps downloaded from the Play Store. The account sharing it does by default to avoid needing to create your own throwaway account is also a potential security risk. It does not come without major drawbacks.
