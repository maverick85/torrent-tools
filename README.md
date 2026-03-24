# torrent-tools
## Userful tools for torrents

### tracker-check
`tracker-check` validates an hash against a list of trackers to let you if the torrent is known by a given tracker, or even if the tracker is up.

#### Installation
- Add the tracker-check file to your `/usr/local/bin/` or `~/.local/bin/` or whatever location suits you.
- Requires `scrapeer` (pip install scrapeer)
- Make the file executable with `chmod +x tracker-check`

#### Usage
Run: `tracker-check -H <hash> -f <tracker-file-location>`

Flags:
- `-H` or `--hash`: The torrent hash
- `-f` or `--file`: The tracker file list. One tracker per line.
- `-r` or `--retries`: retries
- `-t` or `--timeout`: timeout in seconds
- `-o` or `--output`: output file with active trackers
