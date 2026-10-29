# Party Playlist Studio

A browser-based party playlist and DJ mixer.

## Publish with GitHub Pages
1. Open the repository's **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then click **Save**.
4. Wait for GitHub Pages to deploy, then open the URL displayed on that screen.

## Dropbox music library
The app defaults to the Cloudflare Worker at `https://dropbox-bridge.anubhavam23.workers.dev`.

The Worker must have a Cloudflare secret named `DROPBOX_ACCESS_TOKEN`. The browser calls `/songs` to discover MP3s and `/audio?path=...` to stream them. The access token is **not** stored in this repository or in the page source.

## Features
- Refresh the Dropbox song list and load songs into the browser.
- Load local audio files for the current session.
- Build and reorder a dance sequence.
- Set start/end trim points and preview a cut.
- Preview a sequence and export selected ranges to WAV.
- Two DJ decks with volume, playback speed, crossfader and tone pads.

## Notes
- The app is client-side; large tracks may use substantial browser memory.
- Browser audio decoding support varies by format.
- Sequence export is WAV, not MP3.
- Never commit the Dropbox access token to GitHub.
