[🔗](https://github.com/randomwithnoname/security-advice/tree/main/avoid/f-droid.md)

F-Droid has extremely poor security practices and adds a single point of failure for compromising its users by building and signing the apps it distributes. It does not actually protect you from developers since they simply build what's published after antivirus scans.

F-Droid adds another trusted party for each app and has demonstrated that it is extremely careless regarding security and does not take it seriously. They do not follow security best practices or properly maintain the app or infrastructure. They attack things like [app sandboxing](https://source.android.com/docs/security/app-sandbox).

It's far better to use the official releases of the apps from developers obtained without going through F-Droid. Even for the tiny portion of apps F-Droid ships as developer builds, they are still a trusted party for the initial install, and they delay important patches.

You can have privacy and security patches for apps indefinitely delayed until F-Droid sorts out getting their builds for the app working again. There can, and often are, major disagreements with the app developer, resulting in users not receiving updates anymore.

There are other options available. Look into [AppVerifier](https://github.com/soupslurpr/AppVerifier), [Obtainium](https://github.com/ImranR98/Obtainium/blob/main/README.md), and [Accrescent](https://accrescent.app/). F-Droid is not a good fit for people who care about privacy and security. Open source does not make things magically private and secure. Their approach and ideology conflict with those principles.
