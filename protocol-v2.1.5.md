# Agar.io Protocol Version 2.1.5

Agar.io has decided to change their protocol once again. Many extension makers are not happy with the update since all extensions that do not use the newest protocol are broken.

## Server -> client

Every packet that comes from the server starts with a 1 byte header, which indicates the message
type.

### Index
 - [Packet 18](#serverpacket18)



<a name="serverpacket18" href="#serverpacket18"><h4>Packet 18 | Position update?</h4></a>

Tells the client his location

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|16|
|1|4|Int32|Position x|?|
|5|4|Int32|Position y|?|
|9|4|Int32|Token|?|




## Client -> Server


### Index
 - [Packet x](#clientpacketx)

<a name="clientpacketx" href="#clientpacketx"><h4>Packet x | Example</h4></a>
Just an example

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|x|
