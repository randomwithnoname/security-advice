[🔗](https://github.com/randomwithnoname/security-advice/tree/main/avoid/aurora-store.md) Aurora Store simply downloads apps from the Play Store including the Google Play SDK and libraries included in many of the apps. Most of the APKs are generated and signed by Google Play. You aren't avoiding Google Play or hiding the details of your device from them with it.

Aurora Store does not verify the signatures of apps downloaded from the Play Store. The account sharing it does by default to avoid needing to create your own throwaway account is also a potential security risk. It does not come without major drawbacks.

Aurora Store serves an important use case for the people using operating systems that don't support Google Mobile Services (Play Store, Play services), and for users who are using a non-Google certified OS that supports Google Mobile Services and need to use an app such as Netflix which lists itself as using Play Integrity API when it doesn't and thus is not able to be installed via the Play Store on those devices.

For most people, Aurora Store does not serve any legitimate purpose as it does not improve privacy in the way many people think it does. If you need apps that are only available on the Play Store, you should just use the official Play Store app and create an anonymous account just for installing apps if privacy is a concern.

**Aurora Store is not a Google Play Store alternative and does not avoid Google in any meaningful way.**
