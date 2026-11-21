# Breaking AI

A 25-minute talk on adversarial attacks against AI systems: their origin in 2013, attacks across every modality (text, images, audio, video, LiDAR), modern GenAI and LLM attacks (data poisoning, memorization, prompt injection), decision models, and why security and safety belong in your evals. 31 slides, about 22 minutes, grouped by type of AI system: classifiers and decision models, physical attacks, transformers and agents, then defences.

## Promo video

[![Breaking AI promo video](promo/breaking_ai_promo_cover.jpg)](promo/breaking_ai_promo.mp4)

**[Watch or download the promo video (MP4, 72 s, 4:5)](https://github.com/elcronos/breaking-ai-talk/raw/main/promo/breaking_ai_promo.mp4)**

Breaking AI: How to Hack Intelligent Systems. AI Disrupt Summit 2026, West Tech Fest. Saturday 12 December 2026, 11:05 AM, Curtin University, Bentley. Every attack in the video is based on real research or the speaker's own experiments; 3D scenes are labelled as illustrations. Music generated with ElevenLabs.

## Present

Open `breaking_ai_v2_standalone.html` in Chrome. It is a single self-contained file and works offline.

| Key | Action |
|---|---|
| Right arrow / Space / click | next step |
| Left arrow | previous step |
| N | presenter notes and timers |
| R | replay the current slide |
| F | fullscreen |
| M | reduced motion |
| B | blank screen |

On a phone, use the on-screen arrows or swipe. Add `#11` to the URL to jump to slide 11, or `#11-2` for slide 11 after two clicks.

## Reproduce the sticker experiment

One printed sticker reading "DENTED BOX" flips a refund decision on Gemini Decision 1. The photo is staged and this is not any retailer's system.

```
cd reproduce
export GEMINI_API_KEY=...        # your own key
pip install requests
python3 sticker_test.py parcel_clean.jpg     # intact  (damaged 0.02)
python3 sticker_test.py parcel_dented.jpg    # damaged (damaged 0.75)
```

Measured again on 19 November 2026. The same sticker did not flip TypeSafe Jev 1.13 (damaged about 0.2 to 0.3). Only test systems you own or have permission to test.

Camilo Pestana, PhD
