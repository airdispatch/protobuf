# airdispatch/protobuf

This repository contains the canonical protocol buffers used by the
AirDispatch protocol to serialize data to and from the wire.

For creating an AirDispatch implementation in a new language, first
use `protoc` to generate the language-specific serialization files for
you to use from this repository.

## File Information

1. `containers.proto` - Holds definitions for objects that wrap data
   for secure transmission over the wire. These objects provide places
   for the message signature, encryption keys, and message headers.

2. `data.proto` - Holds the definitions for actual user-visible
   objects that can be transmitted inside of containers. These
   currently include mail, raw data (for messages and data >64kb), and
   errors.

3. `server.proto` - Holds definitions for messages pertinent to
   servers handling transferring of messages.

4. `tracker.proto` - Holds definitions that allow tracking servers to
   deliver public keys to the network.
