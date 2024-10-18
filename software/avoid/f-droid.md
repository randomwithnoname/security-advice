[🔗](./f-droid.md)

F-Droid has extremely poor security practices and adds a single point of failure for compromising its users by building and signing the apps it distributes. It does not actually protect you from developers since they simply build what's published after antivirus scans.

F-Droid adds another trusted party for each app and has demonstrated that it is extremely careless regarding security and does not take it seriously. They do not follow security best practices or properly maintain the app or infrastructure. They attack things like [app sandboxing](https://source.android.com/docs/security/app-sandbox).

It's far better to use the official releases of the apps from developers obtained without going through F-Droid. Even for the tiny portion of apps F-Droid ships as developer builds, they are still a trusted party for the initial install, and they delay important patches.

You can have privacy and security patches for apps indefinitely delayed until F-Droid sorts out getting their builds for the app working again. There can, and often are, major disagreements with the app developer, resulting in users not receiving updates anymore.

F-Droid still has problems with their repository system across both the official and unofficial clients. It would be a much better option for apps support self-updating The request install permission allows unattended self-updates for modern apps when using the modern API. 

It's straightforward to include a persistent JobScheduler job for automatic updates which downloads the new APK(s) and installs them as updates. Apps can rely on the standard Android signing key pinning and signature verification. They simply need to verify it's an update, not a new APK.

People can verify initial downloads via the [AppVerifier](https://github.com/randomwithnoname/security-advice/tree/main/use/appverifier.md) app. AppVerifier is published in [Accrescent](https://github.com/randomwithnoname/security-advice/blob/main/use/accrescent.md)., which is an app store distributing official developer builds in a secure way. Accrescent can simply provide filters for open source, reproducible, etc. for people who want it.

[Obtainium](/software/use/obtainium.md) is already a much better option than F-Droid, and has built-in support for AppVerifier. F-Droid is not a good fit for people who care about privacy and security. Open source does not make things magically private and secure. Their approach and ideology conflict with those principles.
