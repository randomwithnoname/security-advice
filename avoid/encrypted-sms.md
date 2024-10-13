[🔗](https://github.com/randomwithnoname/security-advice/tree/main/avoid/encrypted-sms.md)

Silence is an insecure, [dead project](https://git.silence.dev/Silence/Silence-Android/-/tags) and shouldn't be used anymore. It doesn't get security patches. It's a dead fork of Signal which still uses SMS instead of data. The concept is completely obsolete for 4G and beyond where SMS is implemented via TCP/IP using mobile data anyway. It hasn't received updates for years and is missing 
important security patches. 

Deku SMS is a newer, more actively maintained proof-of-concept app which does the same thing as Silence, but I cannot recommend it.

I currently recommend using [Signal](https://signal.org/) and [SimpleX](https://simplex.chat/).
