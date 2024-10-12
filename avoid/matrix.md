[🔗](https://github.com/randomwithnoname/security-advice/blob/main/avoid/matrix.md)

Element has [end-to-end encryption (E2EE)](https://en.wikipedia.org/wiki/End-to-end_encryption), but you can see how much metadata isn't actually encrypted by logging into a new session and not syncing over your keys. The message sender, time, and all other metadata, including emoji reactions to messages, aren't encrypted for E2EE Matrix rooms.

Matrix ONLY encrypts the content field for the messages and attachments. Each server participating in a private E2EE room can see each member of the room, their power level, the permission setup, who sent each message, and when, as well as emoji reactions, etc.

Refer to [this issue](https://github.com/matrix-org/matrix-spec/issues/660) regarding the emoji reaction limitation. It may not seem particularly concerning, but there's a significant amount of sensitive data and metadata beyond just message and attachment content. Each server participating can see this information, which is worse than having only one party privy to it.

Matrix stores the events and messages on each server and syncs them between servers. Each server uses a state resolution algorithm to determine the state of the room based on the events they can see. This can lead to inconsistent states across servers and bugs that may result in bricking.

The decentralized state resolution system creates many of the metadata privacy issues. Servers need to see the entire history of state events to resolve the state of the room.
