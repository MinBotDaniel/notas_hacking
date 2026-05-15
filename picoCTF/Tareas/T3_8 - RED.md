### RED

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/99/flag2of2-final.pdf).

### Solución

┌──(kali㉿kali)-[~/Tareas]
└─$ zsteg -a red.png      
meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 128 colors; 1st RGB space (0), w 0x80, x 0x806, y 0, z 0; 2nd HSB space (1), w 0x100, x 0, y 0xff01, z 0xff
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
b1,rgba,msb,xy      .. file: OpenPGP Public Key
b2,g,lsb,xy         .. text: "ET@UETPETUUT@TUUTD@PDUDDDPE"
b2,rgb,lsb,xy       .. file: OpenPGP Secret Key
b2,bgr,msb,xy       .. file: OpenPGP Public Key
b2,rgba,lsb,xy      .. file: OpenPGP Secret Key
b2,rgba,msb,xy      .. text: "CIkiiiII"
b2,abgr,lsb,xy      .. file: OpenPGP Secret Key
b2,abgr,msb,xy      .. text: "iiiaakikk"
b3,rgba,msb,xy      .. text: "#wb#wp#7p"
b3,abgr,msb,xy      .. text: "7r'wb#7p"
b3p,r,msb,xy        .. text: "{[{_[_[_{_["
b3p,g,lsb,xy        .. text: "%!%! !%!%%%!"
b3p,rgb,lsb,xy      .. file: OpenPGP Secret Key
b3p,bgr,msb,xy      .. text: "ddd``dddd"
b3p,abgr,lsb,xy     .. file: OpenPGP Secret Key
b4,b,lsb,xy         .. file: 0421 Alliant compact executable not stripped
b5p,b,lsb,xy        .. file: PDP-11 separate I&D executable not stripped - version 9
b5p,bgr,lsb,xy      .. file: Excel 8 BIFF 8
b6,rgb,msb,xy       .. file: Applesoft BASIC program data, first line number 126
b6p,b,lsb,xy        .. file: PDP-11 old overlay
b7,g,lsb,xy         .. file: Targa image data - RLE 33088 x 2 x 8 +8192 - right " @\200\002\004"
b8,r,msb,xy         .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,g,lsb,xy         .. file: Targa image data - Map 257 x 257 x 1 +1 "\001\001\001\001\001"
b8,b,lsb,xy         .. file: PDP-11 UNIX/RT ldp
b8,rgb,lsb,xy       .. file: Targa image data - Map (254-65025) 510 x 65281 x 1 +65024 +257 "\376\001\001\377"
b8,bgr,lsb,xy       .. file: PDP-11 UNIX/RT ldp
b8,rgba,lsb,xy      .. file: MySQL table definition file Version 1, MySQL version 16908286
b8,abgr,lsb,xy      .. file: MySQL table definition file Version 1, MySQL version 16908030
b1,bgr,msb,xy,prime .. file: OpenPGP Public Key
b1,rgba,lsb,xy,prime.. text: ".f1!>hD`"
b1,rgba,msb,xy,prime.. text: "gCJ!^U^f{"
b1,abgr,lsb,xy,prime.. text: "!EAUf5A~V"
b1,abgr,msb,xy,prime.. text: "B)F:&eSNmv7"
b2,r,msb,xy,prime   .. text: "}UWWUwU]}"
b2,a,msb,xy,prime   .. text: "W]]WUu_w]]_"
b2,bgr,msb,xy,prime .. file: OpenPGP Public Key
b2,rgba,msb,xy,prime.. text: "AkaCICikck"
b3,rgba,msb,xy,prime.. text: "?b#wp'wp"
b3,abgr,msb,xy,prime.. text: "7r#vb#>b"
b3p,a,msb,xy,prime  .. text: "[{[{{{_{_{[_[[_"
b3p,bgr,lsb,xy,prime.. text: "#&&\"&#''"
b4,b,lsb,xy,prime   .. file: Targa image data - Map (273-273) 256 x 257 x 16 +257 +4352 "\020\021\021\001\001\020\020\021\020\021\020"
b5p,g,lsb,xy,prime  .. file: Excel 8 BIFF 8
b5p,b,lsb,xy,prime  .. file: Targa image data - Map (265-265) 256 x 257 x 8 +257 +2304 "\010\011\011\001\001\010\010\011\010\011\010"
b6,g,msb,xy,prime   .. file: Applesoft BASIC program data, first line number 2
b6,b,msb,xy,prime   .. file: Applesoft BASIC program data, first line number 128
b6p,b,lsb,xy,prime  .. file: PDP-11 UNIX/RT ldp
b6p,bgr,lsb,xy,prime.. file: ctab data
b7,b,lsb,xy,prime   .. file: TTComp archive data, binary, 1K dictionary
b7p,b,lsb,xy,prime  .. file: PDP-11 UNIX/RT ldp
b8,r,msb,xy,prime   .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,g,lsb,xy,prime   .. file: Targa image data - Map (1) 257 x 256 x 1 +257 - 1-bit alpha ""
b8,b,lsb,xy,prime   .. file: raw G3 (Group 3) FAX, byte-padded
b8,rgb,lsb,xy,prime .. file: MySQL table definition file Version 0, MySQL version -16711170
b8,bgr,lsb,xy,prime .. file: raw G3 (Group 3) FAX, byte-padded
b8,rgba,lsb,xy,prime.. file: MySQL table definition file Version 0, MySQL version 16908030
b1,rgba,lsb,yx      .. text: "ffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffff3333333333333333333333333333333333333333333333333333333333333333DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww"                                                                                                                                                                                       
b1,rgba,msb,yx      .. text: ["f" repeated 64 times]
b2,r,msb,yx         .. file: VISX image file
b2,g,lsb,yx         .. file: VISX image file
b2,b,lsb,yx         .. file: VISX image file
b2,a,msb,yx         .. file: VISX image file
b2,rgb,lsb,yx       .. file: OpenPGP Secret Key
b2,bgr,msb,yx       .. file: OpenPGP Public Key
b2,rgba,lsb,yx      .. file: OpenPGP Secret Key
b2,rgba,msb,yx      .. text: ["i" repeated 128 times]
b2,abgr,lsb,yx      .. file: OpenPGP Secret Key
b2,abgr,msb,yx      .. text: "iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKK"                                                                                                                                                                                       
b3,rgba,msb,yx      .. text: "#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r"
b3,abgr,msb,yx      .. text: "#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'"                                                                                                                                                                                       
b3p,r,msb,yx        .. text: ["[" repeated 213 times]
b3p,g,lsb,yx        .. text: "%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%$"
b3p,b,lsb,yx        .. text: "%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% "
b3p,a,msb,yx        .. text: ["[" repeated 42 times]
b3p,rgb,lsb,yx      .. file: AVR firmware, reset at 0x05c5
b3p,bgr,lsb,yx      .. text: "&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\""                                                       
b3p,bgr,msb,yx      .. text: "ddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD"                                                                                                                                                                                       
b3p,abgr,lsb,yx     .. file: AVR firmware, reset at 0x05c5
b3p,abgr,msb,yx     .. text: ["'" repeated 128 times]
b4,a,msb,yx         .. text: ["w" repeated 64 times]
b5p,g,lsb,yx        .. text: ["\t" repeated 64 times]
b5p,b,lsb,yx        .. text: ["\t" repeated 128 times]
b5p,a,lsb,yx        .. file: PC formatted floppy with no filesystem
b5p,a,msb,yx        .. text: ["o" repeated 64 times]
b5p,bgr,lsb,yx      .. text: ["\t" repeated 128 times]
b6p,a,lsb,yx        .. file: MIT scheme (library?)
b6p,a,msb,yx        .. text: ["_" repeated 64 times]
b6p,bgr,msb,yx      .. text: [" " repeated 128 times]
b7p,g,msb,yx        .. file: AVR firmware, reset at 0x00c0
b7p,b,msb,yx        .. file: AVR firmware, reset at 0x00c0
b7p,a,msb,yx        .. text: ["?" repeated 64 times]
b7p,rgb,msb,yx      .. text: ["?" repeated 128 times]
b7p,bgr,msb,yx      .. file: AVR firmware, reset at 0x00c0
b8,a,msb,yx         .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,rgb,lsb,yx       .. file: Targa image data - Map (510-65025) 510 x 65025 x 1 +65025 +257 - 1-bit alpha "\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376"                                                                                         
b8,bgr,lsb,yx       .. file: PDP-11 UNIX/RT ldp
b8,rgba,lsb,yx      .. file: MySQL table definition file Version 1, MySQL version 16908030
b1,rgba,lsb,yx,prime.. text: "fffffffffffffffc33333333333DDDDDDDDDDDwwwwwwwwwwvffffffffl"
b1,rgba,msb,yx,prime.. text: ["f" repeated 15 times]
b1,abgr,lsb,yx,prime.. text: "fffffffffffffffl"
b1,abgr,msb,yx,prime.. text: "fffffffffffffff633333333333DDDDDDDDDDDwwwwwwwwwwgffffffff"
b2,r,msb,yx,prime   .. file: VISX image file
b2,g,lsb,yx,prime   .. file: VISX image file
b2,b,lsb,yx,prime   .. file: VISX image file
b2,a,msb,yx,prime   .. file: VISX image file
b2,rgb,lsb,yx,prime .. file: OpenPGP Secret Key
b2,bgr,msb,yx,prime .. file: OpenPGP Public Key
b2,rgba,lsb,yx,prime.. file: OpenPGP Secret Key
b2,rgba,msb,yx,prime.. text: ["i" repeated 31 times]
b2,abgr,lsb,yx,prime.. file: OpenPGP Secret Key
b2,abgr,msb,yx,prime.. text: "iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiKKKKKKKKKKKKKKKKKKKKKKKaaaaaaaaaaaaaaaaaaaaaakkkkkkkkkkkkkkkkkkkkkiiiiiiiiiiiiiiiiii"
b3,rgba,msb,yx,prime.. text: "#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7"
b3,abgr,msb,yx,prime.. text: "#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#wb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb"
b3p,r,msb,yx,prime  .. text: ["[" repeated 38 times]
b3p,g,lsb,yx,prime  .. text: "%%%%%%%%%% "
b3p,b,lsb,yx,prime  .. text: ["%" repeated 18 times]
b3p,a,msb,yx,prime  .. text: ["[" repeated 10 times]
b3p,rgb,lsb,yx,prime.. file: AVR firmware, reset at 0x05c5
b3p,rgb,msb,yx,prime.. text: ["#" repeated 22 times]
b3p,bgr,lsb,yx,prime.. text: "&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\"\""
b3p,bgr,msb,yx,prime.. text: "dddddddddddddddddddddddddddddddDDDDDDDDDDDDDDDDDDDDDDD``````````````````````ddddddddddddddddddddddddddddddddddddddd"
b3p,abgr,lsb,yx,prime.. file: AVR firmware, reset at 0x05c5
b3p,abgr,msb,yx,prime.. text: ["'" repeated 23 times]
b4,r,msb,yx,prime   .. text: ["w" repeated 57 times]
b4,a,msb,yx,prime   .. text: ["w" repeated 15 times]
b5p,r,lsb,yx,prime  .. file: PC formatted floppy with no filesystem
b5p,r,msb,yx,prime  .. text: ["o" repeated 57 times]
b5p,g,lsb,yx,prime  .. text: ["\t" repeated 15 times]
b5p,b,lsb,yx,prime  .. text: ["\t" repeated 27 times]
b5p,a,lsb,yx,prime  .. file: PC formatted floppy with no filesystem
b5p,a,msb,yx,prime  .. text: ["o" repeated 15 times]
b5p,bgr,lsb,yx,prime.. text: ["\t" repeated 31 times]
b6p,r,lsb,yx,prime  .. file: MIT scheme (library?)
b6p,r,msb,yx,prime  .. text: ["_" repeated 57 times]
b6p,a,lsb,yx,prime  .. file: MIT scheme (library?)
b6p,a,msb,yx,prime  .. text: ["_" repeated 15 times]
b6p,rgb,msb,yx,prime.. text: ["?" repeated 18 times]
b6p,bgr,msb,yx,prime.. text: [" " repeated 23 times]
b7p,r,msb,yx,prime  .. text: ["?" repeated 57 times]
b7p,b,msb,yx,prime  .. file: AVR firmware, reset at 0x00c0
b7p,a,msb,yx,prime  .. text: ["?" repeated 15 times]
b7p,rgb,msb,yx,prime.. text: ["?" repeated 23 times]
b7p,bgr,msb,yx,prime.. file: AVR firmware, reset at 0x00c0
b7p,abgr,msb,yx,prime.. text: ["?" repeated 22 times]
b8,r,msb,yx,prime   .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,a,msb,yx,prime   .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,rgb,lsb,yx,prime .. file: Targa image data - Map (510-65025) 510 x 65025 x 1 +65025 +257 - 1-bit alpha "\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376\001\001\376"                                                          
b8,bgr,lsb,yx,prime .. file: PDP-11 UNIX/RT ldp
b8,rgba,lsb,yx,prime.. file: MySQL table definition file Version 1, MySQL version 16908030
b8,abgr,lsb,yx,prime.. file: MySQL table definition file Version 1, MySQL version 16908030
b1,abgr,msb,XY      .. text: "==QffVTNz4GZ0UzXyBjZfNjc1N2XzQHNtFDdsV3XzgGdfNXMfR2MytnRUN0bjlGc==QffVTNz4GZ0UzXyBjZfNjc1N2XzQHNtFDdsV3XzgGdfNXMfR2MytnRUN0bjlGc==QffVTNz4GZ0UzXyBjZfNjc1N2XzQHNtFDdsV3XzgGdfNXMfR2MytnRUN0bjlGc==QffVTNz4GZ0UzXyBjZfNjc1N2XzQHNtFDdsV3XzgGdfNXMfR2MytnRUN0bjlGc"                                                                                                                                                                                       
b2,r,msb,XY         .. text: "wUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwUwUUuWuUwWwuWuuWwUUUuWUuwUuWWuUwU"                                                                                                                                                                                       
b2,a,lsb,XY         .. file: MPEG ADTS, layer III, v1, 160 kbps, 32 kHz, 2x Monaural
b2,rgba,msb,XY      .. text: "IIiiikIC"
b2,abgr,msb,XY      .. text: "KCciiiiicac"
b3,rgba,msb,XY      .. text: "#7r#7r#7"
b3,abgr,msb,XY      .. text: "vp#7r#7r#wp"
b3p,r,msb,XY        .. text: "{[[[{_[_["
b3p,g,lsb,XY        .. text: "%%%$%$ $%$%$"
b3p,rgb,lsb,XY      .. file: AVR firmware, reset at 0x01e4
b3p,bgr,msb,XY      .. text: "D@`ddddd```"
b4,r,msb,XY         .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b4,g,lsb,XY         .. file: PEX Binary Archive
b4,b,lsb,XY         .. file: PDP-11 UNIX/RT ldp
b5,r,msb,XY         .. file: MPEG ADTS, layer II, v1, 48 kHz, Monaural
b5,b,msb,XY         .. file: Atari DEGAS Elite bitmap 640 x 400 x 2, color palette 0800 8410 4200 0004 1002 ...
b5p,r,msb,XY        .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b5p,g,msb,XY        .. file: PEX Binary Archive
b5p,b,lsb,XY        .. file: PDP-11 UNIX/RT ldp
b5p,bgr,lsb,XY      .. file: Commodore C64 BASIC program, offset 0x0801, line 256, token (0x9), no EOL=0x8, offset 0x0801, line 256, token (0x9)
b5p,abgr,msb,XY     .. file: frozen file 2.1
b6,r,msb,XY         .. file: MPEG ADTS, layer I, v2, 112 kbps, Monaural
b6,g,lsb,XY         .. file: StarOffice Gallery theme \020A\004\020A\004\020A, 1091567681 objects, 1st
b6,g,msb,XY         .. file: Targa image data - RGB 2048 x 8194 x 8 +8322 +33288 - four way interleave ""
b6,b,msb,XY         .. file: Applesoft BASIC program data, first line number 128
b6,rgb,msb,XY       .. file: Applesoft BASIC program data, first line number 124
b6p,r,msb,XY        .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b6p,b,lsb,XY        .. file: PDP-11 UNIX/RT ldp
b6p,bgr,lsb,XY      .. file: Commodore PET BASIC program, offset 0x0401, line 256, token (0x5), offset 0x0401, line 256, token (0x5)
b7,g,lsb,XY         .. file: Targa image data - RLE 33088 x 1024 x 8 +2052 +8208 " @\001"
b7,b,lsb,XY         .. file: TTComp archive data, binary, 1K dictionary
b7,rgb,lsb,XY       .. file: structured file
b7,rgba,lsb,XY      .. file: structured file
b7p,r,msb,XY        .. file: RDI Acoustic Doppler Current Profiler (ADCP)
b7p,b,lsb,XY        .. file: PDP-11 UNIX/RT ldp
b7p,rgb,lsb,XY      .. file: MPEG ADTS, layer II, v1, Monaural
b8,b,lsb,XY         .. file: Adobe Photoshop Color swatch, version 1, 1 colors; 1st RGB space (0), w 0x101, x 0x101, y 0x100, z 0
b8,bgr,lsb,XY       .. file: raw G3 (Group 3) FAX, byte-padded
b1,rgb,lsb,XY,prime .. file: OpenPGP Secret Key
b1,rgba,lsb,XY,prime.. text: "VUsWVdcTFufcGeceEtVCGFdSuV6TCVEtWEdSfUsFcUw5dGFFWFGWWfCwc6SGdDEeTScSvCUFFDeFTWfGevCSdfCVVDGTUv57F4v5FtcetUVge6445TdGUtDFeuTFGg6D6cWtgT6dVdcUTUtfdeWSTsVFveDtVDwfTu5VdDTVu6VtdcG5FGVVEFfeu6CW7GfTSf5SSVCGV4eCtTfFvSVe3UtUVsfWf7DfF6tt7VSuf3CWFDTv5eTEFsdCDFewV5V"
b1,abgr,msb,XY,prime.. text: "=eU7ueF6EdWf6tV6VTGe4tdF5WecE4eTGuTF5fU7d6UwSFtddudtuuf4w6c5tFDTVE565g4UddDVdEuftVg45Ff4eeDtEUgSsdCgSdG6VGUevVcCCSEFtUGDdVWEdtvcDc6uGvEcFeF6UEUGfFVu5E7edgVDGeDwfEWSeFDEeWceGF6tSdteeTdfVWc4ustfE5fS55e4teCV4GEfdg5eV3UGUe7fufsDfdcGGse5Wf34udDEgSVETd7F4DdVweSe"                                                                                                                                                                                       
b2,r,msb,XY,prime   .. text: "WUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUU"                                                                                                                                                                                       
b2,g,lsb,XY,prime   .. text: "ETUTUUETUUEUEQTUUUETTU"
b2,b,lsb,XY,prime   .. text: "UE@AEDEA"
b2,abgr,msb,XY,prime.. text: "KcicckKckciiaiKcaaikciiiKakiciKicackaciaKakaiiacKkcciKicaaKciackackaciacKiicckKaiiKcckkKciaakaiaickaiakckckiiaKkkiKKicKakiaaaaciccacKiKcKkiaKccaiaiaaicaicackiiakickiaKcKiaiiaKciciaaakcacckiKcKkaiKakiKcaikaiKickaccciikicKiKaKaKccaiaakcckaaaaiickccaaiakikKi"
b3,a,msb,XY,prime   .. file: MPEG ADTS, layer I, v2, Monaural
b3,rgba,msb,XY,prime.. text: "#>r#7b#7"
b3,abgr,msb,XY,prime.. text: "7r#7p#wb"
b3p,r,msb,XY,prime  .. text: "_[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[[["                                                                                                                                                                                       
b3p,g,lsb,XY,prime  .. text: "%%!%!%%$%%!%"
b3p,b,lsb,XY,prime  .. text: "!% %!! %"
b3p,rgb,lsb,XY,prime.. file: AVR firmware, reset at 0x01e4
b3p,bgr,msb,XY,prime.. text: "D`d``dD`d`dd`dD```dd`dddD`dd`dDd```d``d`D`d`dd``Dd``dDd```D`d``d``d``d``Ddd``dD`ddD``ddD`d``d`d`d`d`d`d`d`ddd`DdddDDd`D`dd`````d````DdD`Ddd`D```d`d``d``d```ddd`dd`dd`D`Dd`dd`D`d`d```d````ddD`Dd`dD`ddD``dd`dDd`d````dddd`DdD`D`D```d``d``d````dd`d````d`dddDd"
b4,r,msb,XY,prime   .. text: ["w" repeated 255 times]
b4,b,lsb,XY,prime   .. file: PDP-11 UNIX/RT ldp
b5,b,msb,XY,prime   .. file: Atari DEGAS Elite bitmap 640 x 400 x 2, color palette 0800 8400 0208 0184 0000 ...
b5p,r,msb,XY,prime  .. text: ["o" repeated 255 times]
b5p,g,lsb,XY,prime  .. text: ["\t" repeated 10 times]
b5p,b,lsb,XY,prime  .. file: PDP-11 UNIX/RT ldp
b5p,bgr,lsb,XY,prime.. file: Commodore C64 BASIC program, offset 0x0901, line 257, token (0x9), offset 0000, data 0x0001000100ff00ff0001ff0000ff01000100ff00...
b5p,abgr,msb,XY,prime.. file: frozen file 2.1
b6,r,msb,XY,prime   .. file: MPEG ADTS, layer I, v2, 112 kbps, Monaural
b6,b,msb,XY,prime   .. file: Applesoft BASIC program data, first line number 128
b6,a,msb,XY,prime   .. file: ddis/ddif
b6,rgb,msb,XY,prime .. file: Applesoft BASIC program data, first line number 124
b6p,r,msb,XY,prime  .. text: ["_" repeated 255 times]
b6p,b,lsb,XY,prime  .. file: PDP-11 UNIX/RT ldp
b6p,bgr,lsb,XY,prime.. file: Commodore PET BASIC program, offset 0x0501, line 257, token (0x5), offset 0000, data 0x0001000100ff00ff0001ff0000ff01000100ff00...
b7,g,lsb,XY,prime   .. file: Targa image data - RLE 32832 x 1026 x 8 +2052 +8208 - right " @\201\002"
b7,b,lsb,XY,prime   .. file: TTComp archive data, binary, 1K dictionary
b7,rgb,lsb,XY,prime .. file: structured file
b7,rgba,lsb,XY,prime.. file: structured file
b7p,r,msb,XY,prime  .. text: ["?" repeated 255 times]
b7p,b,lsb,XY,prime  .. file: PDP-11 UNIX/RT ldp
b7p,rgb,lsb,XY,prime.. file: MPEG ADTS, layer II, v1, Monaural
b8,g,lsb,XY,prime   .. file: Targa image data - Map 257 x 1 x 1 +257 +257 - 1-bit alpha "\001\001\001\001\001\001\001"
b8,bgr,lsb,XY,prime .. file: raw G3 (Group 3) FAX, byte-padded
b1,rgba,lsb,YX      .. text: ["3" repeated 64 times]
b2,r,msb,YX         .. text: ["U" repeated 32 times]
b2,g,lsb,YX         .. file: VISX image file
b2,b,lsb,YX         .. text: ["U" repeated 32 times]
b2,a,msb,YX         .. text: ["U" repeated 64 times]
b2,rgba,msb,YX      .. file: AVR firmware, reset at 0x0bcb
b2,abgr,lsb,YX      .. file: AVR firmware, reset at 0x07c7
b2,abgr,msb,YX      .. text: ["K" repeated 128 times]
b3,abgr,msb,YX      .. text: "'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'"
b3p,r,msb,YX        .. text: ["[" repeated 42 times]
b3p,g,lsb,YX        .. text: "%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%$"
b3p,b,lsb,YX        .. text: "%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% "
b3p,rgb,msb,YX      .. text: ["'" repeated 128 times]
b3p,bgr,lsb,YX      .. text: ["\"" repeated 128 times]
b3p,bgr,msb,YX      .. text: ["D" repeated 128 times]
b3p,abgr,msb,YX     .. text: ["'" repeated 128 times]
b4,r,msb,YX         .. text: ["w" repeated 64 times]
b5p,r,msb,YX        .. text: ["o" repeated 64 times]
b5p,g,lsb,YX        .. text: ["\t" repeated 64 times]
b5p,b,lsb,YX        .. text: ["\t" repeated 64 times]
b5p,abgr,msb,YX     .. file: old packed data
b6p,r,msb,YX        .. text: ["_" repeated 64 times]
b6p,bgr,msb,YX      .. text: [" " repeated 128 times]
b6p,abgr,msb,YX     .. text: ["?" repeated 128 times]
b7,rgb,lsb,YX       .. file: structured file
b7,rgba,lsb,YX      .. file: structured file
b7p,r,msb,YX        .. text: ["?" repeated 64 times]
b7p,g,msb,YX        .. file: AVR firmware, reset at 0x00c0
b7p,rgb,msb,YX      .. text: ["?" repeated 128 times]
b7p,bgr,msb,YX      .. text: ["@" repeated 128 times]
b8,bgr,lsb,YX       .. file: raw G3 (Group 3) FAX, byte-padded
b1,rgba,lsb,YX,prime.. text: ["3" repeated 11 times]
b1,rgba,msb,YX,prime.. text: "jfffffffffffffffffffffffffffffffffffffffffff"
b1,abgr,lsb,YX,prime.. text: ["f" repeated 43 times]
b1,abgr,msb,YX,prime.. text: "=33333333333"
b2,r,lsb,YX,prime   .. file: AIX core file fulldump 64-bit
b2,r,msb,YX,prime   .. text: ["U" repeated 50 times]
b2,g,lsb,YX,prime   .. file: VISX image file
b2,b,lsb,YX,prime   .. text: "UUUUUUUUUUUUUUUUUUUUUP"
b2,a,msb,YX,prime   .. text: ["U" repeated 21 times]
b2,rgba,msb,YX,prime.. file: AVR firmware, reset at 0x0bcb
b2,abgr,lsb,YX,prime.. file: AVR firmware, reset at 0x07c7
b2,abgr,msb,YX,prime.. text: ["K" repeated 23 times]
b3,rgba,msb,YX,prime.. text: "#>r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#7r#"
b3,abgr,msb,YX,prime.. text: "b'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb'vb"
b3p,r,msb,YX,prime  .. text: "_[[[[[[["
b3p,g,lsb,YX,prime  .. text: "%%%%%%%%%% "
b3p,b,lsb,YX,prime  .. text: ["%" repeated 29 times]
b3p,a,msb,YX,prime  .. text: ["[" repeated 29 times]
b3p,rgb,msb,YX,prime.. text: ["'" repeated 31 times]
b3p,bgr,lsb,YX,prime.. text: ["\"" repeated 23 times]
b3p,bgr,msb,YX,prime.. text: ["D" repeated 23 times]
b3p,abgr,msb,YX,prime.. text: ["'" repeated 23 times]
b4,r,msb,YX,prime   .. text: ["w" repeated 11 times]
b4,a,msb,YX,prime   .. text: ["w" repeated 43 times]
b5p,r,msb,YX,prime  .. text: ["o" repeated 11 times]
b5p,g,lsb,YX,prime  .. text: ["\t" repeated 15 times]
b5p,b,lsb,YX,prime  .. text: ["\t" repeated 11 times]
b5p,a,msb,YX,prime  .. text: ["o" repeated 43 times]
b5p,bgr,lsb,YX,prime.. text: ["\t" repeated 87 times]
b5p,abgr,msb,YX,prime.. file: old packed data
b6p,r,msb,YX,prime  .. text: ["_" repeated 11 times]
b6p,a,msb,YX,prime  .. text: ["_" repeated 43 times]
b6p,bgr,msb,YX,prime.. text: [" " repeated 23 times]
b6p,abgr,msb,YX,prime.. text: ["?" repeated 31 times]
b7,rgb,lsb,YX,prime .. file: structured file
b7,rgba,lsb,YX,prime.. file: structured file
b7p,r,msb,YX,prime  .. text: ["?" repeated 11 times]
b7p,a,msb,YX,prime  .. text: ["?" repeated 43 times]
b7p,rgb,msb,YX,prime.. text: ["?" repeated 23 times]
b7p,bgr,msb,YX,prime.. text: ["@" repeated 23 times]
b7p,abgr,msb,YX,prime.. file: RDI Acoustic Doppler Current Profiler (ADCP)
b8,bgr,lsb,YX,prime .. file: raw G3 (Group 3) FAX, byte-padded
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas]
└─$ echo "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==" | base64 -d
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Tareas]
└─$ echo "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==" | base64 -d                                                                
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}    
### Notas
