### Introduction
The only messaging apps I recommend are [Signal](https://github.com/randomwithnoname/security-advice/blob/main/software/use/signal.md)/[Molly](https://github.com/randomwithnoname/security-advice/blob/main/software/use/molly.md), [SimpleX](https://github.com/randomwithnoname/security-advice/blob/main/software/use/simplex.md). I [don't recommend others](https://github.com/randomwithnoname/security-advice/blob/main/software/avoid/README.md#private-messaging-apps) for the reasons I listed there, but there are also some like [Briar](https://briarproject.org/) or [Cwtch](https://docs.cwtch.im/) which I don't necessarily recommend avoiding, I just don't think they're that useful compared to the other options, especially considering the usability downsides (no iOS app, users need to be online at the same time to communicate).

I do suggest keeping Briar installed in case you have a reason to use it during a catastrophe (no or heavily restricted internet access). Briar and Cwtch route internet traffic via [Tor](https://www.torproject.org/), so if you can use them via the internet, you'll have access to the options I recommend as long as there is servers running. [User-installed apps can be disabled on GrapheneOS](https://grapheneos.org/features#user-installed-apps-can-be-disabled), so I recommend doing that for Briar to prevent it from running while you're not using it.


It's also worth noting that the only instant messaging apps to implement [post-quantum cryptography](https://en.m.wikipedia.org/wiki/Post-quantum_cryptography) are [Signal](https://signal.org/docs/specifications/pqxdh/)/[Molly](https://github.com/randomwithnoname/security-advice/blob/main/software/use/molly.md), [SimpleX](https://simplex.chat/blog/20240314-simplex-chat-v5-6-quantum-resistance-signal-double-ratchet-algorithm.html), [iMessage](https://security.apple.com/blog/imessage-pq3/).

I will be comparing technical features that increase privacy/security as well as other features which lead to better usability for some people. There is an overlap for some features, but I will list privacy/security features under their own categories regardless. Signal implements features in the most private and secure way possible to achieve parity with mainstream options. 

Privacy/security and usability are both very important. In general, if you care about privacy and security, you want to be using the provably most secure technology available, but if said technology is missing features you find useful, then you'll be less likely to use it. This is particularly important when it comes to a communications platform, as it's not only your needs that matter. If you get someone to use a "private and secure" communications app and they have a bad experience, they are unlikely to try a different one in the future, so keep that in mind when choosing.
# Signal vs. Molly
Molly already [lists](https://github.com/mollyim/mollyim-android#features) the features it adds vs. Signal, so I won't repeat those. It does miss some things though.
##### Privacy/security features
- Molly removed support for the [Signal TLS proxy](https://signal.org/blog/help-iran-reconnect/) due to privacy or security issues, so instead added support for a SOCKS5 proxy or Tor via Orbot. I'm not sure exactly what the problem was, but [Tommy Tran](https://tommytran.io/about/) has found [issues](https://privsec.dev/posts/proxies/update-your-signal-tls-proxy/) with the Signal TLS Proxy. The main issue was resolved however. I doubt this was the reason Molly decided to remove it.
##### Other Features
- Molly has an option to hide the calls tab, which will completely hide the navigation bar if stories are disabled.



# Signal vs. SimpleX
*I do not want to push people towards less secure options, but very few people in the information security and cryptography community will ever criticize Signal for that exact reason, maybe it's because [Signal blocks anyone who does](https://x.com/kaepora/status/1810989285148971162), but also the fact there's hasn't been a serious alternative.. until recently.*

Signal is a centralized service that uses phone numbers for account registration, optionally contact discovery and ties them to user accounts. A centralized service isn't inherently a bad thing. It reduces points of failure, but is also a single point of failure, which matters less if you think about it considering we're dependent on the internet service providers which are *a few* points of failure themselves. Traditional federated communications systems (email, XMPP, Matrix, etc) result in worse privacy than a centralized service, regardless of the encryption added on top, due to [metadata](https://en.wikipedia.org/wiki/Metadata) leakage between providers. If everyone ran their own servers, you would have better messaging layer privacy, but this is not a realistic expectation, and doesn't solve transport layer privacy issues unless everyone is using something like [Tor](https://www.torproject.org/), [I2P](https://geti2p.net/en/), etc. which come with their own performance and reliability issues. P2P solutions that don't rely on an overlay network like Tor or I2P are less private than a service ran by another party which is used by many users and implements [end-to-end encryption](https://en.wikipedia.org/wiki/End-to-end_encryption) on the client as you're still reliant on the ISPs not to misuse the data they have about users' activity, and P2P solutions are directly leaking the metadata (IP addresses) of who you're talking to with to the ISPs, and your IP address the people you're talking to, which is a very bad thing if you're trying to stay anonymous. Signal can be used without giving contacts a phone number by using usernames instead, but if you can't trust Signal's servers, they can see which phone nunbers you're communicating with and when, even if both parties only opt to use usernames.

Signal usernames use [Risterro hashes](https://www.zellic.io/blog/signal-username-ristretto-hashes/), which means they cannot simply see a list of usernames registered, but they'd have to know.. or guess the username first. Unfortunately, this is a trivial task with [rainbow tables](https://en.m.wikipedia.org/wiki/Rainbow_table), assuming most people are just using their first name as a username.

[Sealed sender](https://signal.org/blog/sealed-sender/) [does not solve the metadata problems from a technical perspective](https://cs-people.bu.edu/kaptchuk/publications/ndss21.pdf). Signal does have a good track record, but that's if you can trust court cases and the [transcripts they've disclosed of government requests](https://signal.org/bigbrother/). Despite this problem, Signal is still a far better choice than any of the mainstream options. It has properly implemented end-to-end encryption for messages, files, calls which can be [verified](https://support.signal.org/hc/en-us/articles/360007060632-What-is-a-safety-number-and-why-do-I-see-that-it-changed) without trusting a server.

Anyone who can recieve calls/texts to the phone number you registered with can permanently lock you out of your Signal account and impersonate you for contacts that discovered your profile via phone number, assuming they don't verify safety numbers via a different channel (ideally not based on phone numbers) and react to change. The situation is far better now that you've got the option to not use phone numbers for discovery, but getting locked out of your account **permanantly** can still be catastrophic. Anybody who works in security knows that [SIM swapping ](https://www.microsoft.com/en-us/microsoft-365-life-hacks/privacy-and-safety/what-is-sim-swapping) is a very real threat and securing phone numbers can be an impossible task depending on the provider. Signal could still use phone numbers for registration and contact discovery without tying them to accounts.
This discussion doesn't come up in the security comminity, since there isn't a better option.. until recently.

##### Meet SimpleX
SimpleX is a messaging app that *[doesn't](https://github.com/simplex-chat/simplex-chat/tree/stable?tab=readme-ov-file#privacy-and-security-technical-details-and-limitations)* downgrade security vs. Signal. It implements Signal's state-of-the-art double ratchet algorithm which provides forward secrecy and break-in recovery. Anyone can run the servers, but you should avoid that if you want network layer privacy. It's best to stick with the ones that come preset by the app as they've had good reliability in the past, are unlikely to shutdown, have the most users which makes you blend in more. It's a matter of control vs. privacy.
##### Privacy/security features
- Phone numbers aren't used for account creation and therefore can't be used to discover contacts. You need to share an invite link which can be presented in the form of a QR code.
- Invite links/QR code contain public keys so users don't need to manually verify security code to prevent MITM from SimpleX servers. The option is still there to detect MITM from the channel the link was sent over.
##### Other features
- Signal has stories like on Snapchat, etc. SimpleX doesn't.
- Signal has built-in gifs and stickers. SimpleX doesn't, however a keyboard app can still provide them.
- Signal has group calls. SimpleX doesn't.
- Signal has a built-in image editor. SimpleX doesn't.
- Signal has a calls tab which shows your history of calls made within Signal, as well as making it easier for people who struggle to navigate their phone to initiate calls.
## SimpleX vs. Molly
- SimpleX allows you to set a manual database passphrase rather than relying on Keystore on Android or Keychain or iOS. On desktop, it prompts you to set a manual passphrase during the setup, but you can optionally use a random passphrase which is stored in a text file. Molly has a list of commonly used passwords and will block you from using them and any other weak passwords. Molly also has an option to automatically lock the database if you've not unlocked it for a certain amount of time. SimpleX has that option for it's SimpleX Lock feature, which lets you lock the app with your device unlock method (PIN, biometrics, etc) or a separate PIN. That is not encrypting the database, and it has no rate limit so any determined non-technical attacker can bypass it.

- RAM shredding needs to be clarified. There is an [open issue](https://github.com/simplex-chat/simplex-chat/issues/4407) about it.

- SimpleX has limited multi-device support in the first place. Profiles on the mobile app can be used from a desktop on the same LAN, but not at the same time.

- Block unknown contacts is not applicable at all in SimpleX. Only people you choose to connect with by sharing an invite link can contact you. Invite links can be deleted and you won't lose any contacts/groups you've already connected to.

- Call history is purged with disappearing messages in SimpleX.

- There is no option to disable debug logs in SimpleX. It needs to be clarified.

- There is no option to schedule backups in SimpleX. It needs to be done manually.

- SimpleX has built-in support for using a SOCKS proxy, including Tor provided by another app like Orbot or InviZible Pro.

- SimpleX does not support UnifiedPush. Work is being put into improving the current system instead as UnifiedPush would only have a benefit if you have multiple apps using the same channel. [UnifiedPush adoption is extremly low](https://unifiedpush.org/users/apps/).
