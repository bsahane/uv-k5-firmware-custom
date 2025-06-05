## NUNU Protocol

This firmware since `v.21.0` incorporates message hopping mesh network functionality called the **"NUNU Protocol"**.

> [!TIP]
> You can download early beta NUNU Protocol release [here](https://www.patreon.com/posts/public-early-98088972).


Which allows to extend the range of infrastructure-less communications via intermediate stations (nodes).

This way of communications can also be described as [flooding](https://en.wikipedia.org/wiki/Flooding_(computer_networking)).

The protocol is based on the [Meshtastic principles](https://meshtastic.org/docs/overview/mesh-algo).

## Videos

For a quick explanation of Meshtastic please check out video below:

[![Meshtastic algorithm](https://img.youtube.com/vi/7v6UbC5blJU/0.jpg)](https://www.youtube.com/watch?v=7v6UbC5blJU)

Video of the NUNU Protocol showing message hopping with 3 radios:

https://github.com/kamilsss655/uv-k5-firmware-custom/assets/8842065/5392ce36-9308-4a54-a92c-a82474b4b0d5

Video of the NUNU Protocol with 4 radios:

https://github.com/kamilsss655/uv-k5-firmware-custom/assets/8842065/078dca54-b9aa-4930-bf19-0529c1c1791b

## Functionalities

NUNU Protocol implements:
* [Carrier-Sense Multiple Access with Collision Avoidance](https://en.wikipedia.org/wiki/Carrier-sense_multiple_access_with_collision_avoidance)
  * the radio will not TX if the line is busy to avoid collisions
  * if the line is busy the radio will wait with TX for the random amount of time, until the line is free
  * of course there might be a case when 2 radios TX at the same time because they didn't hear each other (also known as the [hidden node problem](https://en.wikipedia.org/wiki/Hidden_node_problem)).
* [CRC codes](https://en.wikipedia.org/wiki/Cyclic_redundancy_check) to determine if packet has been corrupted in transit
  * all messages with incorrect CRC codes are ignored
  * this is a vital part of the protocol as it prevents hopping incorrect packets through the mesh network
* Give and take approach
  * Users can only request that their messages be hopped if they contribute to the network by hopping messages for others
  * controlled via the `MsgAck` menu option
* Encryption is supported
  * The nodes that receive encrypted packets without having the right encryption key will not understand them, but will still hop them forward
  * This enables communities to share the mesh network and still have ability to have both public and private conversations
* Hopping state which once entered
  * drops all incoming packets
  * prevents user sending new messages

## Packet structure

Packet structure:
| Size (in bytes) | Name | Description |
| --- | --- | --- |
| 4 | sync word | Sync word for this FW `0x30 0x72 0x57 0x6C` |
| 1 | header | Packet header |
| 30 | payload | Packet payload (can be encrypted) |
| 13 | nonce | Packet nonce used for encryption |
| 8 | crc | Error detecting code (based on the display hash function) |

Header structure:
| Size (in bits) | Name | Description |
| --- | --- | --- |
| 5 | type | Header type |
| 3 | hop | Hop count (max 7 hops) |

Header types:
| Value | Name | Description |
| --- | --- | --- |
| 0 | MESSAGE_PACKET | Unencrypted message |
| 1 | ENCRYPTED_MESSAGE_PACKET | Encrypted message |
| 2 | INVALID_PACKET | Invalid packet, headers greater and equal to this one as treated as invalid packets |