# [F-Droid](https://github.com/randomwithnoname/security-advice/tree/main/avoid/f-droid.md)

F-Droid has extremely poor security practices and adds a single point of failure for compromising their users through them building and signing the apps they distribute. It does not actually protect you from developers since they simply build what's published after antivirus scans...

F-Droid adds another trusted party for each app and has demonstrated they're extremely careless in regards to security and do not take it seriously. They do not follow security best practices or properly maintain the app or infrastructure. They attack things like [app sandboxing](https://source.android.com/docs/security/app-sandbox)

It's far better to use the official releases of the apps from developers obtained without going through F-Droid. Even for the tiny portion of apps F-Droid ships developer builds, they're still a trusted party for the initial install and they delay important patches.

You can have privacy/security patches for apps indefinitely delayed until F-Droid sorts out getting their builds for app working again. There can and often are major disagreements with the app developer resulting in users not getting updates anymore.

There are other options available. Look into [AppVerifier](https://github.com/soupslurpr/AppVerifier), [Obtainium](https://github.com/ImranR98/Obtainium/blob/main/README.md) and [Accrescent](https://accrescent.app/). F-Droid is not a good fit for people who care about privacy and security. Open source does not make things magically private and secure. Their approach and ideology conflicts with those things.
