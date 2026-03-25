# torrent-tools
## Userful tools for torrents

### tracker-check
`tracker-check` validates an hash against a list of trackers to let you if the torrent is known by a given tracker, or even if the tracker is up.

#### Installation
- Add the tracker-check file to your `/usr/local/bin/` or `~/.local/bin/` or whatever location suits you.
- Requires `scrapeer` (`pip install scrapeer`)
- Requires `bencodepy` (`pip install bencodepy`)
- Make the file executable with `chmod +x tracker-check`

#### Usage
Run: `tracker-check -H <hash>`

Flags:
- `-H` or `--hash`: The torrent hash
- `-f` or `--file`: Optional: The tracker file list. One tracker per line.
- `-r` or `--retries`: Optional: retries
- `-t` or `--timeout`: Optional: timeout in seconds
- `-o` or `--output`: Optional: output file with active trackers
