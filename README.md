# Game Library

The revised components file depends on the revised version of the map below.
Note that the "beenthere" variable takes three values.

false = present location
true =  been there
null =  never been there

 {
      "rooms": 
      [
        {
          "name": "A",
          "north": "D",
          "east": "B",
          "south": null,
          "west": null,
          "entrance": "south",
          "beenthere": null
        },
        {
          "name": "B",
          "north": "E",
          "east": "C",
          "south": null,
          "west": "A",
          "entrance": "null",
          "beenthere": false

        },
        {
          "name": "C",
          "north": null,
          "east": null,
          "south": null,
          "west": "B",
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "D",
          "north": "G",
          "east": null,
          "south": "A",
          "west": null,
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "E",
          "north": null,
          "east": "F",
          "south": "B",
          "west": null,
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "F",
          "north": null,
          "east": null,
          "south": null,
          "west": "E",
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "G",
          "north": "H",
          "east": null,
          "south": "D",
          "west": null,
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "H",
          "north": null,
          "east": "I",
          "south": "G",
          "west": null,
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "I",
          "north": null,
          "east": "J",
          "south": null,
          "west": "H",
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "J",
          "north": null,
          "east": "K",
          "south": null,
          "west": "I",
          "entrance": "null",
          "beenthere": null

        },
        {
          "name": "K",
          "north": null,
          "east": null,
          "south": null,
          "west": "J",
          "entrance": "null",
          "beenthere": null, 
          "treasure": true
        }
        
      ]









Game library for JavaScript course.

> This repository is for learning purposes. It may intentionally contain bugs or
fail to function properly. The code may be purposefully difficult to read,
contain syntax errors, or only be a partial solution. You should not base code
off of this and absolutely should not use it in production.

You can use this to print a map from a game file. For instance:

```javascript
// app.js
console.log(require('jsi-gamelib').map(require(process.argv[2])));
```

Now you can run `node app.js game.json` to produce:

    +---------+---------+---------+---------+
    |         |         |         |         |
    |    H         I         J         K    |
    |         |         |         |         |
    +---   ---+---------+---------+---------+
    |         |                              
    |    G    |                              
    |         |                              
    +---   ---+---------+---------+          
    |         |         |         |          
    |    D    |    E         F    |          
    |         |         |         |          
    +---   ---+---   ---+---------+          
    |         |         |         |          
    |    A         B         C    |          
    |         |         |         |          
    +---------+--  ^  --+---------+          

The game file format looks like this (this file was used to produce the above
map):

    {
      "rooms": [
        {
          "name": "A",
          "north": "D",
          "east": "B",
          "south": null,
          "west": null
        },
        {
          "name": "B",
          "north": "E",
          "east": "C",
          "south": null,
          "west": "A",
          "entrance": "south"
        },
        {
          "name": "C",
          "north": null,
          "east": null,
          "south": null,
          "west": "B"
        },
        {
          "name": "D",
          "north": "G",
          "east": null,
          "south": "A",
          "west": null
        },
        {
          "name": "E",
          "north": null,
          "east": "F",
          "south": "B",
          "west": null
        },
        {
          "name": "F",
          "north": null,
          "east": null,
          "south": null,
          "west": "E"
        },
        {
          "name": "G",
          "north": "H",
          "east": null,
          "south": "D",
          "west": null
        },
        {
          "name": "H",
          "north": null,
          "east": "I",
          "south": "G",
          "west": null
        },
        {
          "name": "I",
          "north": null,
          "east": "J",
          "south": null,
          "west": "H"
        },
        {
          "name": "J",
          "north": null,
          "east": "K",
          "south": null,
          "west": "I"
        },
        {
          "name": "K",
          "north": null,
          "east": null,
          "south": null,
          "west": "J",
          "treasure": true
        }
      ]
    }
