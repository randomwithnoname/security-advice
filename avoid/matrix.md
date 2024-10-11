# [Element (Matrix)](https://github.com/randomwithnoname/security-advice/blob/main/avoid/matrix.md)
Element has [end-to-end encryption (E2EE)](https://en.wikipedia.org/wiki/End-to-end_encryption) but you can see how much metadata isn't actually encrypted by logging into a new session and not syncing over your keys. Message sender, time and all other metadata including emoji reactions to messages aren't encrypted for E2EE Matrix rooms..

Matrix ONLY encrypts the content field for the messages and the attachments. Each server participating in a private E2EE room can see each member of the room, their power level, the permission setup, who sent each message and when, emoji reactions, etc.

See [this issue](https://github.com/matrix-org/matrix-spec/issues/660) about the emoji reaction limitation. It may not seem particularly bad, but there's really a whole lot of sensitive data/metadata aside from message/attachment content. Each server participating can see it, which is worse than only 1 party seeing it.

Matrix stores the events/messages on each server and syncs them between the servers. Each server uses a state resolution algorithm to determine the state of the room based on the events they can see. Servers end up with inconsistent state and there are bugs leading to bricking.

The decentralized state resolution system results creates a lot of the metadata privacy issues. Servers need to see the whole history of state events to resolve the state of the room. 
