# Reddit

Check each sidebar for self-promo rules and required flair. Use the weekly self-promo thread where a sub requires it. Space posts 2h+ apart.

## r/NewTubers
Why: small creators need subtitles and are price-sensitive.
**Title:** Made a free tool that generates SRT subtitles without uploading your video anywhere
**Body:**
I got tired of paying for subtitle tools just to caption short videos, so I built one that runs entirely in the browser. You drop your video in, the Whisper AI model runs on your own computer, and you get an SRT file you can upload straight to YouTube or import into CapCut/Premiere.

It's free for videos up to 10 minutes, which covers most uploads here. The first run downloads the model (~80 MB) and it's cached after that.

Honest limitation: on older laptops without a decent GPU it's slower than the paid cloud tools.

https://barbhuiya12.github.io/hushscribe/

What editor do you use? I want to check the SRT imports cleanly everywhere.

## r/podcasting
Why: podcasters transcribe every episode for show notes and SEO.
**Title:** How are you all handling episode transcripts without a monthly subscription?
**Body:**
I've been transcribing recordings and didn't love the idea of uploading guest conversations to a cloud service, so I built a browser tool that runs Whisper locally. Nothing is uploaded; you can disconnect from the internet after it loads.

Free covers 10 minutes per file; full episodes need a one-time Pro unlock (not a subscription). It exports plain text for show notes and SRT/VTT for video podcasts.

No speaker labels yet. That's the next thing I'm building, and I know it matters for interviews.

https://barbhuiya12.github.io/hushscribe/

Would speaker labels be the deciding feature for you, or is it accuracy?

## r/GradSchool
Why: qualitative researchers transcribe interviews under ethics/privacy rules.
**Title:** For anyone transcribing research interviews under IRB privacy constraints
**Body:**
A lot of transcription services upload your audio to their servers, which can be a problem when your consent forms say data stays local. I built a tool where the speech model (OpenAI's open-source Whisper) runs inside your browser, so the recording never leaves your machine.

You get timestamps and a text export; clicking a line jumps to that point in the audio, which makes checking accuracy faster.

It's a new project and not a certified compliance tool, so check with your IRB. But technically, nothing is transmitted.

https://barbhuiya12.github.io/hushscribe/

What's your current workflow for cleaning up transcripts?

## r/webdev
Why: the tech itself (WebGPU + Whisper in a worker) is interesting to devs.
**Title:** Running Whisper on WebGPU in a Web Worker: lessons from building a no-backend transcriber
**Body:**
I built a transcription app as a single static page: Transformers.js loads Whisper, runs it in a module Web Worker on WebGPU (WASM fallback), and streams segments back per 30-second window.

Things I learned:
- `AudioContext({ sampleRate: 16000 })` + `decodeAudioData` resamples video/audio for you in one call.
- q4 decoder + fp32 encoder was the sweet spot on WebGPU.
- Fixed 30s windows are simple but can clip words at boundaries.

Code: https://github.com/Barbhuiya12/hushscribe
Demo: https://barbhuiya12.github.io/hushscribe/

Has anyone done overlapping windows without doubling compute?
