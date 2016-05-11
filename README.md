##Agar.io Protocol

Agar.io has decided to change their protocol once again. Many extension makers are not happy with the update since all extensions that do not use the newest protocol are broken.

### Index
 - [Protocol V2.1.5](protocol-v2.1.5.md)

### Reverse engineer techniques

To determine how the protocol is built you could use one of the following techniques:

 - Replace window.WebSocket with [code from pastebin](http://pastebin.com/Ykx4LRDh) to listen between data that gets received and send.
 - Create an server and let it connect to your server with agar.io?ip=yourserverip:port to see what you receive.
