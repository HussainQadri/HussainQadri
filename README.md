# Hussain Qadri

First-year Computer Science student at King's College London. I like building
things where the details matter: systems code, financial protocols, developer
tools, signal processing, and small technical experiments that force me to learn
the underlying idea properly.

## What I am working on

### [FIXEngine](https://github.com/HussainQadri/FIXEngine)

A C++20 implementation of a small FIX engine, starting from the wire format and
building upward. It currently parses FIX 4.2 messages, validates body length and
checksum fields, loads the XML dictionary with `pugixml`, resolves tag and enum
metadata, and wraps several admin messages in typed classes.

The next layer is session behaviour: sequence numbers, logon/logout state,
heartbeats, resend flow, persistence, and transport.

### [Rabab Tuner](https://github.com/HussainQadri/rabab-tuner)

A browser-based tuner for the Rabab, built with React and Flask. The app captures
microphone audio, estimates pitch, and gives cent-level feedback against sargam
note targets.

I started with FFT-based detection, then moved toward a YIN-style pitch pipeline
after running into the usual problems with harmonics, noisy recordings, and the
strongest spectral peak not always being the fundamental frequency.

### [EncodeEd](https://github.com/HussainQadri/EncodeEd)

My A-level Computer Science project: a Python/PyQt5 desktop app for exploring
lossless compression algorithms. It implements RLE, Huffman Coding,
Shannon-Fano, LZW, Arithmetic Coding, and LZ77 with visual explanations and
runtime plots.

The point was not to make a production compressor. It was to make the mechanics
of each algorithm visible.

## Writing

I keep project notes, implementation writeups, and side quests on my site:

**[hussainqadri.github.io](https://hussainqadri.github.io/)**

Recent topics include building a FIX dictionary validator, improving pitch
detection for the Rabab tuner, walking through EncodeEd, and refining my Neovim
setup.

