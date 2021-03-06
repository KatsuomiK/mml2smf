# MML to Standard MIDI File converter

This utility is created for in-development MIDI synthesizer [synthesis.js](https://github.com/korinVR/synthesis.js), but it can be used for general use cases.

The features are very limited for now.

## Usage

### From command line

```bash
$ npm install -g mml2smf

$ mml2smf test.mml
$ mml2smf test.mml -o output.mid
$ mml2smf -m cdefg -o test.mid
$ mml2smf -m "t140 o5l8q7 ccggaag4 ffeeddc4; o4l8 cgegcgeg >b<gfg>b<gc4" -o test.mid
```

### From JavaScript

```js
import mml2smf from 'mml2smf'

const smf = mml2smf('cdefg') // returns Uint8Array
```

## MML ([Music Macro Language](https://en.wikipedia.org/wiki/Music_Macro_Language))

command|MML
-------|---
Notes|c, d, e, f, g, a, b, +, -
Octave|o\[octave\], &lt;, &gt; (4)
Note Length|l\[note length\] (4)
Tempo|t\[tempo\]
Gate Time|q\[1-8\] (6)
Velocity|u\[0-127\] (100)
Channel Volume|v\[0-127\]
Pan|p\[-64-63\]
Expression Controller|E\[0-127\]
Program Change|@\[0-127\]
Control Change|B\[0-119\],\[0-127\]
Channel Aftertouch|D\[0-127\]
Key Shift|k\[-127-127\] (0)
Set MIDI Channel|C\[1-16\] (1)
Next Track and MIDI Channel|;
Tie|^
Comment|//..., /\*...\*/

## Development

To launch:

```bash
$ npm start
```

To test:

```bash
$ npm test
```

# License

MIT

# Author

Katsuomi Kobayashi ([@korinVR](https://twitter.com/korinVR) / [@korinVR_en](https://twitter.com/korinVR_en))

https://framesynthesis.com/

