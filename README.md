# Left! Left! LEFT! — Spacewar co-op

Play the Windows playtest build with a friend using Steam's Spacewar app identity. This project packages a small, build-specific change to the game's existing Steam integration.

**[Download v0.1.0](https://github.com/j117mw3/LeftLeftLEFT-Spacewar/releases/download/v0.1.0/LeftLeftLEFT-Spacewar-v0.1.0.zip)**

## Requirements

- The installed Windows x64 playtest, Steam build **26172243**. Both players need the same game build and package version.
- Steam running and two separate Steam accounts.
- An original `GameAssembly.dll` with SHA-256 `b81c064eabebbc0b30af66f9684df3ffbae5e8a515e76a813c95a5ca95158f2e`.

## Install

1. Close the game and keep Steam running.
2. Open your playtest folder containing `LeftLeftLEFT.exe`. Back up `GameAssembly.dll` and any existing `steam_appid.txt` somewhere outside that folder.
3. Extract the download into that folder and replace `GameAssembly.dll` when prompted.
4. Launch `LeftLeftLEFT.exe` normally. Create a lobby and invite your friend.

The disabled Steam playtest Play button is not restored. No installer, launcher, or launch arguments are needed.

## Testing and troubleshooting

The author reports a successful two-player co-op session. Steam initialization under app 480 and lobby creation were also observed in the local log. Third-player handling, disconnect/rejoin, host departure and progression remain unverified.

If the game cannot initialize Steam, make sure Steam is running and that the package is next to the game executable. Check `%USERPROFILE%\AppData\LocalLow\Stellux Interactive\LeftLeftLEFT\Player.log` for the `[SteamLobby]` message. Stop at startup errors before testing invitations.

If an invitation fails, first confirm the host has created a lobby, then try the in-game friend list or Steam overlay. Both players should verify they use the same build and package. Logs can contain personal information; remove identifiers before sharing them.

## Uninstall

Close the game and restore the original `GameAssembly.dll` from your backup. Restore your previous `steam_appid.txt`, or remove it if the package added it. Verify the restored DLL hash against the value above. Do not remove unrelated game files.

## License and attribution

The original project documentation is licensed under MIT; see [LICENSE](LICENSE). The modified game-derived DLL is not covered by that license and remains subject to its rights holder's terms. This is an unofficial project and is not affiliated with the game's developer or Valve.
