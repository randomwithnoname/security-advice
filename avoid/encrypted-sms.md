[🔗](https://github.com/randomwithnoname/security-advice/tree/main/avoid/encrypted-sms.md)

Silence is an insecure, [dead project](https://git.silence.dev/Silence/Silence-Android/-/tags) and shouldn't be used anymore. It doesn't get security patches. It's a dead fork of Signal which still uses SMS instead of data. The concept is completely obsolete for 4G and beyond where SMS is implemented via [TCP/IP](https://en.m.wikipedia.org/wiki/Internet_protocol_suite) using mobile data anyway. It hasn't received updates for years and is missing 
important security patches. 

Deku SMS is a newer, more actively maintained proof-of-concept app which does the same thing as Silence, but I cannot recommend it.

There are also some other services which claim to provide encrypted/secure SMS. Magic doesn't exist. Both people need to be using the same or a compatible app to use [end-to-end encryption.
](https://en.m.wikipedia.org/wiki/End-to-end_encryption) That also applies to Deku and Silence.

I currently [recommend](https://github.com/randomwithnoname/security-advice/blob/main/use/README.md#private-messaging-apps) using [Signal](https://signal.org/)/[Molly](https://github.com/randomwithnoname/security-advice/blob/main/use/molly.md) and [SimpleX](https://simplex.chat/).
