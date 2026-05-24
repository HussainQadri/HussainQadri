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
metadata, and wraps several admin messages in typed classes. Right now, this is the current project I am mainly placing focus on. It's very much still in the early stages.

The next layer is session behaviour: sequence numbers, logon/logout state,
heartbeats, resend flow, persistence, and transport.

### [Rabab Tuner](https://github.com/HussainQadri/rabab-tuner)

A browser-based tuner for the Rabab, built with React and Flask. The app captures
microphone audio, estimates pitch, and gives cent-level feedback against sargam
note targets.

I started with FFT-based detection, then moved toward a YIN-style pitch pipeline
after running into the usual problems with harmonics, noisy recordings, and the
strongest spectral peak not always being the fundamental frequency.

### [Sift](https://github.com/HussainQadri/sift)

A Rust semantic code search engine built around Tree-sitter and vector retrieval.
It ingests source directories, extracts function-level records with source
locations, embeds full function bodies using a code-oriented model, and searches
a persisted local index from natural-language queries.

The current search path uses exact cosine similarity as a correctness baseline.
I am working toward a custom HNSW approximate nearest-neighbour index, with
latency and recall benchmarks against exhaustive search for large codebases.

## Writing

I keep project notes, implementation writeups, and side quests on my site:

**[hussainqadri.github.io](https://hussainqadri.github.io/)**
