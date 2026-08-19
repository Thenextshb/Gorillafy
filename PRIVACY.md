# Privacy Policy — Gorillafy

Last updated: 2026-08-19

Gorillafy is a Gorilla Tag mod that adds a Spotify remote and a soundboard to the in-game menu. This page explains what data it touches and where it goes.

## Spotify data

Gorillafy uses Spotify's official Web API with the OAuth 2.0 PKCE flow to let you control your own Spotify playback from inside the game (play/pause, skip, seek, volume, search, and viewing your playlists).

- Sign-in happens directly between your PC and Spotify's servers (`accounts.spotify.com`). Gorillafy never sees or stores your Spotify password.
- After you sign in, Spotify issues a refresh token. That token is saved **only on your own computer**, in your BepInEx config folder (`spotify_refresh_token.txt`), so you don't have to sign in every time you launch the game.
- The token is used solely to call the Spotify Web API on your behalf (now-playing status, search, playback control). It is never sent anywhere except Spotify's own API.
- No Spotify data — account info, listening activity, search queries, playlists — is collected, logged, or transmitted to any server operated by the mod's developer or any third party.

## Local files

- Custom soundboard audio files live in a `Sounds` folder next to the game, created locally. These files never leave your computer except when a sound is played, which is sent through the game's existing voice chat so other players in the room can hear it — the same way your microphone audio already works.
- Controller button bindings for the soundboard are stored locally in `gorillafy_binds.txt`.
- Your saved audio output device name is stored locally in `gorillafy_speaker.txt`.

## Third-party services contacted

- `accounts.spotify.com` / `api.spotify.com` — Spotify sign-in and playback control.
- `api.github.com` — checks the latest released version number so the mod can tell you when an update is available. No personal data is sent with this request.
- `myinstants.com` — opened in your browser only if you tap "Get Sounds"; Gorillafy does not communicate with it directly.

## Data retention and removal

Everything described above is stored locally on your own machine. To remove it, delete `spotify_refresh_token.txt`, `spotify_device.txt`, `gorillafy_binds.txt`, and `gorillafy_speaker.txt` from your BepInEx config / game folder, and revoke Gorillafy's access at any time from your [Spotify account app permissions](https://www.spotify.com/account/apps/).

## Contact

Questions about this policy can be raised as an issue on the [Gorillafy GitHub repository](https://github.com/Thenextshb/Gorillafy).
