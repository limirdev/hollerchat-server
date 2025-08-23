# hollerchat-server
Distributed server for hollerchat

### Thoughts
* Use Signal protocol for encryption?
* How to trust a new server
  * Transitive trust?
  * Central authentication?

## Holler protocol
JSON messages supporting three levels: public, group and private.

### Public message
```json
{
  "scope": "PUBLIC",
  "audience": [],
  "message": "This is a public message with markdown :smiley:",
  "images": []
}
```
### Group message
```json
{
  "scope": "GROUP",
  "audience": ["grouphash"],
  "message": "This is a group message with markdown :fire:",
  "images": []
}
```
### Private message
```json
{
  "scope": "PRIVATE",
  "audience": ["userhash1@server", "userhash2@server", ...],
  "message": "This is a **private** message with markdown :cat:",
  "images": []
}
``` 
