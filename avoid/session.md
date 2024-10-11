# [Session](https://github.com/randomwithnoname/security-advice/tree/main/avoid/session.md)

Session stopped using the industry standard [Signal protocol](https://en.m.wikipedia.org/wiki/Signal_Protocol) (used Facebook Messenger, Google Messages, WhatsApp) and has lost [Perfect Forward Secrecy (PFS) ](https://en.m.wikipedia.org/wiki/Forward_secrecy) and [deniability](https://en.m.wikipedia.org/wiki/Deniable_authentication).

Perfect Forward Secrecy means that even if an attacker gets the encrypted messages and later compromises your device to get your main keys, they can't get the messages which no longer have session keys on your device.

Session losing deniability doesn't matter to most people and isn't very practical until official versions of messaging apps allow you to create fake messages on your end. PFS is important though.
