# Hussain Qadri

First-year Computer Science student at King's College London. I like building
things where the details matter: systems code, financial protocols, developer
tools, signal processing, and small technical experiments that force me to learn
the underlying idea properly.

## What I am working on

### [Sift](https://github.com/HussainQadri/sift)

A Rust semantic code search engine built around Tree-sitter and vector retrieval.
It ingests source directories, extracts function-level records with source
locations, embeds full function bodies using a code-oriented model, and searches
a persisted local index from natural-language queries.

The current search path uses exact cosine similarity as a correctness baseline.
I have built the single-layer navigable graph that will form the base of a
custom HNSW approximate nearest-neighbour index. The next steps are adding the
hierarchical layers and measuring its latency and recall against exhaustive
search on real codebases.

### [FIXEngine](https://github.com/HussainQadri/FIXEngine)

A C++20 implementation of a small FIX engine, starting from the wire format and
building upward. It parses FIX 4.2 messages, validates body length and checksum
fields, loads the XML dictionary with `pugixml`, resolves tag and enum metadata,
and provides typed wrappers for core admin messages.

The initial session layer tracks logon/logout state and sequence numbers, builds
outbound admin messages, responds to test requests, and detects sequence gaps.
The next stages are heartbeat scheduling, resend and gap-fill replay,
persistence, and TCP transport.

### [Rabab Tuner](https://github.com/HussainQadri/rabab-tuner)

A browser-based tuner for the Rabab, built with React and Flask. The frontend
captures raw microphone audio through the Web Audio API and streams PCM chunks
to the backend over Socket.IO. A custom YIN pitch-detection pipeline estimates
the fundamental frequency and returns cent-level feedback against sargam note
targets.

I originally used FFT peak detection, but moved to YIN after harmonics, noisy
recordings, and string resonances made the strongest spectral peak an unreliable
estimate of pitch. The streaming pipeline replaced the earlier record-and-upload
flow to make tuning feedback more responsive.

## Writing

I keep project notes, implementation writeups, and side quests on my site:

**[hussainqadri.github.io](https://hussainqadri.github.io/)**
