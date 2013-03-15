ID3Writer
=========

A JavaScript library for writing mp3 ID3 Tags. The ID3 Tags are in version 2.3.

Usage
-----

You can use ID3Writer like this:
```JavaScript
var blob = ID3Writer.create([
                              {frameType: 'TIT2', data: "DVNO"},
                              {frameType: 'TALB', data: "†"},
                              {frameType: 'TPE1', data: "Justice"},
                              {frameType: 'TYER', data: "2007"},
                              {frameType: 'APIC', data: "<Any kind of binary data>", coverMime: "image/png"}
                            ], "<Any kind of binary data>");
                               // The actual mp3 data comes as second argument of the "create" function
```

The encoding of text is always UTF-8. If you want to store a frame with binary data – except for the cover, which is handled specifically – you can use the optional argument ```isBinary: true``` for this frame.

**Have fun!**
