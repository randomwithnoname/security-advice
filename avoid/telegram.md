# [Telegram](https://github.com/randomwithnoname/security-advice/tree/main/avoid/telegram.md)
Telegram is not an [end-to-end encrypted (E2EE)](https://en.wikipedia.org/wiki/End-to-end_encryption) messaging app and has access to the vast majority of private messages on the platform. It also stores a lot of interesting data beyond that about users.

Telegram has no E2EE support for groups or regular direct messages, only an unnecessarily crippled form of secret chat direct messages they hide away in a menu and discourage using. Hardly qualifies as an E2EE messaging app based on having that...

Telegram has full access to all of the content of group chats and regular one-to-one chats due to lack of end-to-end encryption. Their opt-in secret chats use homegrown end-to-end encryption with weaknesses. Deleting the content from the app likely won't remove all copies of it.

Telegram has heavily participated in misinformation campaigns targeting actual private messaging apps with always enabled, properly implemented end-to-end encryption such as Signal. Should stop getting any advice from anyone who told you to use Telegram as a private messenger.

A major example of how Telegram's opt-in secret chat encryption has gone seriously wrong before: https://words.filippo.io/dispatches/telegram-ecdh/.

Apps like [Signal](https://signal.org/) and [SimpleX](https://simplex.chat/) can't access messages, media and profiles. Telegram has access to all content in private group chats and regular private messages unless people used a secret chat. They can automatically scan it, moderate and provide data to authorities based on it.
