[🔗](./molly.md)

[Molly](https://github.com/mollyim/mollyim-android#download) is a [fork](https://en.m.wikipedia.org/wiki/Fork_(software_development)) of [Signal](./signal.md) for Android which comes with various security and usability improvements.

Molly is updated every two weeks to include the latest features and bug fixes from Signal. The exceptions are security issues, which are patched as soon as fixes become available.

Aside from the features listed on [its README](https://github.com/mollyim/mollyim-android#features), it also lets you hide the calls tab which completely hides the navigation bar when stories are disabled, and the MobileCoin wallet has been removed.

Molly can also be installed alongside Signal, which means you can use 2 Signal accounts without needing to use an Android Work Profile or Private Space. However, you cannot register your account on both apps at the same time. Molly as a linked device though, so it can be used while the primary device (app) is offline. Only the primary app registered will remain active, and the other will go offline. 

If you are currently a Signal user and want to use Molly instead of Signal (with the same phone number), see [Migrating From Signal](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal) on the Molly wiki.

Molly connects to Signal's production server, so you can chat with your Signal contacts seamlessly..

Molly has 3 variants. Molly, Molly-FOSS, Molly-UP. Molly and Molly-FOSS share the same package name, so they cannot be installed together. For example, if you installed Molly then installed Molly-FOSS, Molly-FOSS would simply be installed as an update to Molly and you would keep your user data. Molly-UP can be installed alongside Molly/Molly-FOSS.

[Here is this official comparison of dependencies (functionality)
](https://github.com/mollyim/mollyim-android#dependency-comparison).

Molly-UP supports UnifiedPush, which can act as an open-source replacement to Google's Firebase Cloud Messaging (FCM) for apps that suppprt it. Unfortunately, Signal doesn't support UnifiedPush, so Molly had to make a workaround (MollySocket) which involves a server that acts as a linked device without any encryption keys. It's not difficult to setup a MollySocket server, but it's also not a one click process. There are publicly available MollySocket servers, but you're relying on them to provide a reliable service. [adminForge offers a MollySocket server](https://adminforge.de/services/mollysocket/), and they have a good track record for uptime and reliability.

[Molly-UP is merging with Molly soon](https://github.com/mollyim/mollyim-android/pull/368), and they plan to deprecate Molly-UP, so I wouldn't recommend installing it at this point unless you're going to setup Molly-UP as a linked device until its deprecated, as account registrations [cost Signal a lot of money over time.
](https://signal.org/blog/signal-is-expensive/)

I recommend [obtaining Molly via Accrescent](https://accrescent.app/app/im.molly.app).
