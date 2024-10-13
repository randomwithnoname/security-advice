[🔗](https://github.com/randomwithnoname/security-advice/blob/main/use/molly.md)

[Molly](https://github.com/mollyim/mollyim-android#download) is a [fork](https://en.m.wikipedia.org/wiki/Fork_(software_development)) of [Signal](https://github.com/randomwithnoname/security-advice/tree/main/use/signal.md) for Android which comes with various security and usability improvements.

Aside from the features listed on [its README](https://github.com/mollyim/mollyim-android#features), it also lets you hide the calls tab which completely hides the navigation bar when stories are disabled. 

Molly can also be installed alongside Signal, which means you can use 2 Signal accounts without using an Android Work Profile or Private Space.

Molly connects to Signal's production servers, so you can seamlessly chat with contacts who use Signal.

Molly has 3 variants. Molly, Molly-FOSS, Molly-UP. Molly and Molly-FOSS share the same package name, so they cannot be installed together. For example, if you installed Molly then installed Molly-FOSS, Molly-FOSS would simply be installed as an update to Molly and you would keep your user data. Molly-UP can be installed alongside Molly/Molly-FOSS.

[Here is this official comparison of dependencies (functionality)
](https://github.com/mollyim/mollyim-android#dependency-comparison).

Molly-UP supports UnifiedPush, which can act as an open-source replacement to Google's Firebase Cloud Messaging (FCM) for apps that suppprt it. Unfortunately, Signal doesn't support UnifiedPush, so Molly had to make a workaround (MollySocket) which involves a server that acts as a linked device without any encryption keys. It's not difficult to setup a MollySocket server, but it's also not a one click process. There are publicly available MollySocket servers, but you're relying on them to provide a reliable service. [adminForge offers a MollySocket server](https://adminforge.de/services/mollysocket/), and they have a good track record for uptime and reliability.

[Molly-UP is merging with Molly soon](https://github.com/mollyim/mollyim-android/pull/368), and they plan to deprecate Molly-UP, so I wouldn't recommend installing it at this point unless you're going to setup Molly-UP as a linked device until its deprecated, as account registrations [cost Signal a lot of money over time.
](https://signal.org/blog/signal-is-expensive/)

I recommend [obtaining Molly via Accrescent](https://accrescent.app/app/im.molly.app).
