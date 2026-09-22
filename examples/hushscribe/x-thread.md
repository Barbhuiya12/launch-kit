# X thread

1/ (160)
I built an Otter.ai alternative where your audio never leaves your laptop.

Whisper AI runs inside a browser tab. No upload. No server. No subscription.

Demo 👇
[GIF: drop video → transcript streams in → click line → video jumps]

2/ (170)
The problem: every transcription tool wants you to upload private recordings (interviews, meetings, client calls) to their servers, then charge monthly for the privilege.

3/ (195)
Hushscribe: drop an audio or video file and get a timestamped transcript plus SRT/VTT subtitles. 90+ languages. Click any line to jump to that moment.

Turn Wi-Fi off after it loads. Still works.

4/ (163)
How: Transformers.js loads Whisper (~80 MB, cached once) into a Web Worker. It runs on your GPU via WebGPU, or falls back to CPU. The whole app is one static page.

5/ (111)
Who it's for: YouTubers who need subtitles, podcasters writing show notes, researchers with private interviews.

6/ (140)
Free up to 10 min per file. Pro is one-time, not a subscription.

Try it: https://barbhuiya12.github.io/hushscribe/

What should I add next?
