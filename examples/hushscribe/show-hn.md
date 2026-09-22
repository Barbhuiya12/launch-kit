# Show HN

**Title** (75 chars)
Show HN: Hushscribe – Whisper transcription and subtitles, fully in-browser

**Link:** https://barbhuiya12.github.io/hushscribe/

**Maker's first comment**

I wanted subtitles for a few recorded interviews, but every tool I found wanted me to upload the audio and pay monthly. The recordings were private, so I built this instead.

How it works: the page loads Whisper (base, ~80 MB, cached after first load) through Transformers.js and runs it in a Web Worker. It uses WebGPU when available and falls back to WASM on the CPU. Audio is decoded with the Web Audio API at 16 kHz and fed in 30-second windows, so the transcript streams in as it goes. Output is SRT, VTT or plain text, and you can click a line to seek the player. There is no backend; it's a static page.

Rough edges:
- I cut audio into fixed 30s chunks, so a word that lands exactly on a boundary can get clipped. Overlapping strides would fix it at some speed cost.
- The CPU fallback is slow on older laptops.
- Very long videos are decoded fully into memory.

What I'd love feedback on: is chunk-boundary clipping noticeable on your recordings, and would you trade speed for overlapping windows?

Free for files up to 10 minutes. A one-time Pro unlock covers longer files and the larger model.
