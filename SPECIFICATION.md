# descent specification

current descent is in very early development and the main concepts still just
exist within my (mokytis's) mind. in this file i'm going to try as best as i can
to get those ideas down in text, and then build a reference implentation in
golang.

## core concepts

### descentalised

descent is decentralised. that means that any two users should be able to
communicate without relying on any descent based code, but that running on the
sender and recipiants device. other nodes may be used to cache messages when
another node isn't online (this is configurable per conversation).

### anonymous

descent is designed with anonimity at heart. this means that only you and the
person you are talking to should be able to know who each other are. descent is
designed as a tor hidden service (HS) allowing us to hide who it is you are
talking to. users are identified purely by their v3 `.onion` address.

### private

descent is private. that means that nobody expect you and the message rescipiant
should be able to see the content of messages you send. messages are encrypted
using AES keys with expiery times configurable per conversation (see message
encryption) allowing other trusted nodes to cache AES encrypted messages sent to
you while you are offline.
