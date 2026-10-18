# Channel 6 — YouTube Automation Pipeline (`multipost6`)

Cloud-native, 100% automated YouTube video upload, metadata optimization, comment responder, and analytics pipeline running exclusively on GitHub Actions.

## Channel Overview
- **Owner Account:** `shehryarali2963@gmail.com`
- **GitHub Account:** `shehryarali2963-rgb`
- **Channel Title:** `Michaela McDermott`
- **Channel ID:** `UC7J-3Bnj2t3G0FpfypNleJA`
- **Current Total Videos:** 33 (First automated upload verified live)
- **Target Cadence:** 3 uploads / day (1 video per scheduled workflow run)
- **Execution Target:** 100% cloud-hosted on GitHub Actions (`ubuntu-latest`). User PC is completely OFF.

## Live Verification & Production Proof
- **First Live Video Upload:** [https://youtu.be/_zyj4xX4o6Q](https://youtu.be/_zyj4xX4o6Q)
- **Video Title:** `Generations Connecting: Sweet Grandfather and Baby Moment`
- **Privacy Status:** `public`
- **Upload Status:** `processed`
- **Made for Kids:** `False`
- **Runner Host OS:** `ubuntu-latest` (Linux 6.8 / Ubuntu 24.04)
- **Runner Public IP:** `172.182.226.16`

## Cloud Architecture & Storage
- **Google Cloud Project:** `yt-multipost-channel6`
- **Drive Inbox Folder ID:** `1uML-O9C7DVMIXHYzWENf8tJ8qQstADuE`
- **Drive Uploaded Archive Folder ID:** `1UNKIRhBSjjCiCE7YRpC34GzIRHGaTO5Z`
- **GitHub Pages & Privacy Policy:** `https://shehryarali2963-rgb.github.io/privacy.html`

## Automated Workflows
1. **Daily Upload (`.github/workflows/daily-upload.yml`)**:
   - **Schedule:** `15 4,10,16 * * *` (09:15, 15:15, 21:15 PKT / 04:15, 10:15, 16:15 UTC)
   - Fetches oldest video from Drive inbox, encodes to vertical 1080x1920 (Shorts), generates AI metadata via Gemini, uploads to YouTube (Public), archives video into `Uploaded` folder, and commits state with `[skip ci]`.
2. **Comment Replies (`.github/workflows/comment-replies.yml`)**:
   - **Schedule:** `0 17 * * *` (22:00 PKT / 17:00 UTC)
   - Scans recent video comments and crafts contextual AI responses.
3. **Weekly Analytics (`.github/workflows/weekly-analytics.yml`)**:
   - **Schedule:** `0 18 * * 0` (Sunday 23:00 PKT / 18:00 UTC)
   - Generates weekly view, watch time, and subscriber performance report.
