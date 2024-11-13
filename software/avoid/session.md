[🔗](./session.md)

Session stopped using the industry-standard [Signal protocol](https://en.m.wikipedia.org/wiki/Signal_Protocol), therefore has lost [Perfect Forward Secrecy (PFS)](https://en.m.wikipedia.org/wiki/Forward_secrecy) and [deniability](https://en.m.wikipedia.org/wiki/Deniable_authentication).

Perfect Forward Secrecy means that even if an attacker gets the encrypted messages and later compromises your device to obtain your main keys, they can't access the messages that no longer have session keys on your device.

The loss of deniability in Session doesn't matter to most people and doesn't have much of a practical downside until official versions of messaging apps allow you to create fake messages on your end. PFS is important, though.

This means you could genuinely use Facebook Messenger, Google Messages, WhatsApp, and iMessage more securely. All of these come with their own issues, such as encouraging users to back up their messages to cloud storage without end-to-end encryption, mixing encrypted private chats with unencrypted chats, and lacking proper verification UI.

You should just tell people to get [Signal](https://github.com/randomwithnoname/security-advice/tree/main/use/signal.md). [SimpleX](https://simplex.chat/) is a good option if Signal doesn't meet your needs.
