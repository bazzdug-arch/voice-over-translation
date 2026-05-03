## What's Changed

Added cloud.mail.ru video translation support. This fork extends the original VOT extension to work with public video files hosted on Mail.ru Cloud.

### Changes

- New site support: cloud.mail.ru - translate videos from public Mail.ru Cloud links
- CloudMailRuHelper: extracts direct MP4 download URL via window.cloudSettings.dispatcher.weblink_get
- Detected language: defaults to en (English) for cloud.mail.ru since it is a file hosting service without language metadata
- Added cloud.mail.ru and datacloudmail.ru to connect permissions for CORS

### Installation

1. Download vot.user.js below
2. Install in Tampermonkey/Violentmonkey (open the file in browser)
3. Or load vot-extension-chrome zip as unpacked extension in Chrome

### Usage

1. Open a public cloud.mail.ru link with a video file
2. Click the .mp4 file to open the video player
3. The VOT translation button should appear on the player
4. Click it to get Russian voice-over translation

### Known Limitations

- Requires the video to be in a public shared link (no auth)
- Yandex VOT API must be able to follow the 301 redirect from weblink_get URL - if translation fails, this may need a fix in the helper
- 4-hour video length limit (Yandex API)
- Source language defaults to English - change manually if video is in another language

### Based on

- ilyhalight/voice-over-translation v1.11.5
- FOSWLY/vot.js v2.4.17
