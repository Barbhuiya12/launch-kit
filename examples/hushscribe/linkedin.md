# LinkedIn
(Put the link in the first comment, not the post.)

I stopped uploading private recordings to transcription services.

So I built a tool where the AI runs on your own laptop instead.

Here's the problem I kept hitting:
Interviews, client calls, lecture recordings. Every transcription tool wanted me to upload them to a server and pay monthly.

What I built: Hushscribe.
→ Drop in audio or video
→ Whisper AI runs inside your browser
→ Get a transcript + subtitles (SRT/VTT)
→ Nothing is ever uploaded

What I learned building it:
1. Browsers can now run real AI models on the GPU (WebGPU). A static web page can do what used to need a server.
2. Privacy is a feature people can verify. Turn Wi-Fi off and it still works.
3. The simplest architecture (no backend) is also the cheapest to run. Hosting costs $0.

It's free for files up to 10 minutes.

Link in the first comment. I'd love to hear what you'd use it for.

#AI #Privacy #WebDevelopment
