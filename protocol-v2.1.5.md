# Agar.io Protocol Version 2.1.5

Agar.io has decided to change their protocol once again. Many extension makers are not happy with the update since all extensions that do not use the newest protocol are broken.

## Server -> client

### Init keys

First two authorisation tokens
 
    new Int8Array([-2,6,0,0,0]);
    new Int8Array([-1,-78,-86,42,-87]);

## Server -> client

Every packet that comes from the server starts with a 1 byte header, which indicates the message
type.

### Index
 - [Packet 18 | Reset playercells](#serverpacket18)
 - [Packet 32 | Cell Ids](#serverpacket32)
 - [Packet 49 | LeaderBoard](#serverpacket49)
 - [Packet 64 | Viewport](#serverpacket64)
 - [Packet 255 | Cells update](#serverpacket255)



<a name="serverpacket18" href="#serverpacket18"><h4>Packet 18 | Reset playercells</h4></a>

Resets all playercells their location and id. Probably used to try to patch bots.

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|18|
|?|?|?|?|?|

<a name="serverpacket32" href="#serverpacket32"><h4>Packet 32 | Cell Ids</h4></a>


|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint32|Packet ID|32|
|?|?|?|?|?|

<a name="serverpacket49" href="#serverpacket49"><h4>Packet 49 | LeaderBoard</h4></a>

Top 10 dominating cells.

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|49|
|?|?|?|?|?|


<a name="serverpacket64" href="#serverpacket64"><h4>Packet 64 | Viewport</h4></a>

Tells the client his viewport

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|64|
|?|?|?|?|?|

<a name="serverpacket255" href="#serverpacket255"><h4>Packet 255 | Cells update</h4></a>

Tells the client his viewport

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|255|
|?|?|?|?|?|


## Client -> Server


### Index
 - [Packet 0 | Nickname / Spawn](#clientpacket0)
 - [Packet 16 | Update movement](#clientpacket16)
 - [Packet 102 | Facebook / Google+ token](#clientpacket102)

<a name="clientpacket0" href="#clientpacket0"><h4>Packet 0 | Nickname / Spawn</h4></a>

Login with facebook / Google+ token

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|16|
|1|?|?|?|?|

<a name="clientpacket16" href="#clientpacket16"><h4>Packet 16 | Update movement</h4></a>

Tells the server his direction

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|16|
|1|4|Int32|Position x|?|
|5|4|Int32|Position y|?|
|9|4|Int32|Token|?|


<a name="clientpacket102" href="#clientpacket102"><h4>Packet 102 | Facebook / Google+ token</h4></a>

Login with facebook / Google+ token

|offset|Bytes|Data Type|Description|Default|
|------|-----|---------|-----------|-------|
|0|1|Uint8|Packet ID|16|
|1|?|?|?|?|
