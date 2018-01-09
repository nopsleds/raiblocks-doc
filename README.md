# Raiblocks - doc


This repo / document aims at gathering functional and technical info about the Raiblocks crypto-currency project.


## Resources

* Raiblock website - https://raiblocks.net/


## Protocol

### Message Header

- 2 bytes => magic number
- 1 byte => version max
- 1 byte => version using
- 1 byte => version min
- ? bytes => message type
- 2 bytes => extensions (bitset)


### Message "Keep-Alive"

#### Payload

list of IPV6 address (16 bytes) + port (2 bytes) of all known peers

#### Processing

reinit peer list ???!!!


### Message "Publish"
#### Payload

contains a 'block' >> deserialize_block (...)

#### Processing

- hold proof of work that needs validation



### Messages "Confirm Req"
#### Payload

contains a 'block' >> deserialize_block (...)

#### Processing

- hold proof of work that needs validation


### Messages "Confirm Ack"
#### Payload

- vote.account
- vote.signature
- vote.seq
- block >> deserialize_block (...)

#### Processing

- hold proof of work that needs validation

### Message "Frontier Req"

#### Payload
