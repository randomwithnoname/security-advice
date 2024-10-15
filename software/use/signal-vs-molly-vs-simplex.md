### Introduction
The only messaging apps I recommend are [Signal](https://github.com/randomwithnoname/security-advice/blob/main/software/use/signal.md)/[Molly](https://github.com/randomwithnoname/security-advice/blob/main/software/use/molly.md), [SimpleX](https://github.com/randomwithnoname/security-advice/blob/main/software/use/simplex.md). I [don't recommend others](https://github.com/randomwithnoname/security-advice/blob/main/software/avoid/README.md#private-messaging-apps) for the reasons I listed there, but there are also some like [Briar](https://briarproject.org/) or [Cwtch](https://docs.cwtch.im/) which I don't necessarily recommend avoiding, I just don't think they're that useful compared to the other options, especially considering the usability downsides (no iOS app, users need to be online at the same time to communicate).

I do suggest keeping Briar installed in case you have a reason to use it during a catastrophe (no or heavily restricted internet access). Briar and Cwtch route internet traffic via [Tor](https://www.torproject.org/), so if you can use them via the internet, you'll have access to the options I recommend as long as there is servers running. [User-installed apps can be disabled on GrapheneOS](https://grapheneos.org/features#user-installed-apps-can-be-disabled), so I recommend doing that for Briar to prevent it from running while you're not using it.


It's also worth noting that the only instant messaging apps to implement [post-quantum cryptography](https://en.m.wikipedia.org/wiki/Post-quantum_cryptography) are [Signal](https://signal.org/docs/specifications/pqxdh/)/[Molly](https://github.com/randomwithnoname/security-advice/blob/main/software/use/molly.md), [SimpleX](https://simplex.chat/blog/20240314-simplex-chat-v5-6-quantum-resistance-signal-double-ratchet-algorithm.html), [iMessage](https://security.apple.com/blog/imessage-pq3/).

I will be comparing technical features that increase privacy/security as well as other features which lead to better usability for some people. There is an overlap for some features, but I will list privacy/security features under their own categories regardless. Signal implements features in the most private and secure way possible to achieve parity with mainstream options. 

Privacy/secutity and usability are both very important. In general, if you care about privacy and security, you want to be using the provably most secure technology available, but if said technology is missing features you find useful, then you'll be less likely to use it. This is particularly important when it comes to a communications platform, as it's not only your needs that matter. If you get someone to use a "private and secure" communications app and they have a bad experience, they are unlikely to try a different one in the future, so keep that in mind when choosing.
# Signal vs. Molly
##### Privacy/security features

Molly already [lists](https://github.com/mollyim/mollyim-android#features) the features it adds vs. Signal, so I won't repeat that. It does miss some things though.
- Molly removed support for the [Signal TLS proxy](https://signal.org/blog/help-iran-reconnect/) due to privacy or security issues, so instead added support for a SOCKS5 proxy or Tor via Orbot. I'm not sure exactly what the problem was, but [Tommy Tran](https://tommytran.io/about/) has found [issues](https://privsec.dev/posts/proxies/update-your-signal-tls-proxy/) with the Signal TLS Proxy. The main issue was resolved however. I doubt this was the reason Molly decided to remove it.


- Back in 2018, Signal allowed the user to set a passphrase to secure the local message database. But this option was removed with the introduction of file-based encryption on Android. Molly brings it back again with [additional security features](https://github.com/mollyim/mollyim-android/wiki/Data-Encryption-At-Rest).

- Molly securely shreds sensitive data from RAM. It needs to be clarified what this does, but I assume this is so that keys for database encryption are cleared from memory when the database is locked so forensics can't recover them.

- If database encryption is enabled, you can set a device lock timeout so the database will automatically. The timer can be anywhere from 0 secomds to 99 hours, 99 minutes, 99 seconds...

- Molly allows you to block unknown contacts, which will block messages and calls from unknown senders for security and anti-spam. This feature is a less compelling reason to use Molly over Signal useful since the instruction of usernames, but if an adversary that knows your Signal username is a threat, then you may find it useful.

- Android logs can be disabled, which can potentially prove privacy against future device access, depending on your setup.

- Molly used to have its own feature for deleting contacts, but Signal has since added their own implementation of this feature and Molly has removed theirs.

- Call history will be removed along with disappearing messages in Molly, unlike Signal.
##### Other Features
- Signal supports using miltiple devices with the same account, but the only mobile devices it supports linking are iPads. Molly can be setup as a linked device rather than a primary device. It can also be used on Android tablets.

- Molly has an option to hide the calls tab, which will completely hide the navigation bar if stories are disabled.

- Molly allows you to schedule backups between a daily or weekly interval and the number of backups to retain.



# Signal vs. SimpleX
Signal is a centralized service that uses a phone numbers for registration and ties them to user accounts. A centralized service isn't inherently a bad thing. It reduces points of failure, but is also a single point of failure, which matters less if you think about it considering we're dependent on the internet service providers which are *a few* points of failure themselves. Traditional federated communications systems (email, XMPP, Matrix, etc) result in worse privacy than a centralized service, regardless of the encryption added on top, due to [metadata](https://en.wikipedia.org/wiki/Metadata) leakage between providers. If everyone ran their own servers, you would have better messaging layer privacy, but this is not a realistic expectation, and doesn't solve transport layer privacy issues unless everyone is using something like Tor, I2P, etc. which come with their own performance and reliability issues. P2P solutions that don't rely on an overlay network like Tor or I2P are less private than a service ran by another party which is used by many users which implements end-to-end encryption on the client as you're still reliant on the ISPs not to misuse the data they have about users' activity, and P2P solutions are directly leaking the metadata of who you're talking to with to the ISPs as well as the people you're talking to, which is a very bad thing if you're trying to stay anonymous. Signal can be used without giving contacts a phone number by using usernames instead, but if you can't trust Signal's servers, they can see who you're communicating with and when. [Sealed sender](https://signal.org/blog/sealed-sender/) [does not solve the metadata problems from a technical perspective](https://cs-people.bu.edu/kaptchuk/publications/ndss21.pdf). Signal does have a good track record, that's if you can trust court cases and the [transcripts they've disclosed of government requests](https://signal.org/bigbrother/).

I do not want to push people towards less secure options, but lying about Signal's limitations is not productive if you want it to improve. Very few people in the security community speak up about this. It's time it stopped. Signal blocks security researchers who criticize them. This 

Anyone who can recieve calls/texts to the phone number you registered with can permanently lock you out of your Signal account and impersonate you for contacts that discovered your profile via phone number, assuming they don't verify safety numbers via a different channel (ideally not based on phone numbers) and react to change. The situation is far better now that you've got the option to not use phone numbers for discovery, but getting locked out of your account **permanantly** can still be catastrophic. Anybody who works in security knows that [SIM swapping ](https://www.microsoft.com/en-us/microsoft-365-life-hacks/privacy-and-safety/what-is-sim-swapping) is a very real threat and securing phone numbers can be an impossible task depending on the provider.


# SimpleX vs. Molly
