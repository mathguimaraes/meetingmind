# MeetingMind

A macOS menu-bar app that automatically detects your meetings, records mic + system audio, transcribes everything locally on-device, and gives you an AI summary and action items — no manual start/stop, no cloud audio upload.

- **Auto-detection** — starts recording when it detects a meeting (Zoom, Meet, Teams, …), ends automatically when it's over.
- **Local transcription** — [WhisperKit](https://github.com/argmaxinc/WhisperKit) runs entirely on-device (Apple Silicon Neural Engine). Your audio never leaves your Mac unless you opt into cloud summaries.
- **Speaker split** — separates what *you* said from what others said, so summaries and insights are attributed correctly.
- **AI summaries & insights** — bring your own [Gemini API key](https://aistudio.google.com/apikey) (free tier is plenty) for cloud summaries, or run a fully local model (Qwen/Llama, via [MLX](https://github.com/ml-explore/mlx)) with no key at all.
- **Daily report** — a recap of each day's meetings and the tasks that came out of them, right on the home screen.

## Requirements

- Apple Silicon Mac (M1 or later)
- macOS 13.0+

## Install

1. Download the latest `MeetingMind.dmg` from [Releases](https://github.com/mathguimaraes/meetingmind/releases/latest).
2. Open the DMG and drag **MeetingMind** into **Applications**.
3. Launch it. macOS will ask for **Microphone** and **Screen Recording** permission (the latter is what captures other participants' audio — it's what triggers the purple recording-indicator dot, that's normal and required).
4. Click the menu-bar icon → **Settings** to add a Gemini API key (optional — needed only for cloud AI summaries; everything else works without one).

The app checks for updates automatically (via [Sparkle](https://sparkle-project.org)) — you'll be notified in-app when a new version is available.

## Privacy

Audio and transcripts are stored locally on your Mac. Nothing is sent anywhere unless you explicitly enable a cloud AI provider for summaries — and even then, only the *text transcript* is sent to that provider's API, never raw audio.

## Feedback / Issues

Use **menu bar icon → Send Feedback…** in the app, or open an [issue](https://github.com/mathguimaraes/meetingmind/issues) here.
