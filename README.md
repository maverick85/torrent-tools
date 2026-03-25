# torrent-tools
## Userful tools for torrents

### tracker-check
`tracker-check` validates a torrent against a list of trackers to let you if the torrent is known by a given tracker, or even if the tracker is up.

#### Installation
- Add the tracker-check file to your `/usr/local/bin/` or `~/.local/bin/` or whatever location suits you.
- Requires `scrapeer` (`pip install scrapeer`)
- Requires `bencodepy` (`pip install bencodepy`)
- Make the file executable with `chmod +x tracker-check`

#### Usage
usage: tracker-check [-h] (-H HASH | -T TORRENT) [-I] [-f FILE] [-t TIMEOUT] [-r RETRIES] [-o OUTPUT]
tracker-check: error: one of the arguments -H/--hash -T/--torrent is required

`tracker-check -H <hash>`: scrapes an hash against the torrent list
`tracker-check -T <torrent> -I`: Prints torrent information
`tracker-check -T <torrent>`: Extracts the torrent hash and scrapes against the tracker list

Flags:
- `-H` or `--hash`: Torrent hash
- `-T` or `--torrent`: Torrent file
- `-I` or `--info`: Extract torrent info (Used with `-T`/`--torrent`)
- `-f` or `--file`: Optional: The tracker file list. One tracker per line.
- `-r` or `--retries`: Optional: retries
- `-t` or `--timeout`: Optional: timeout in seconds
- `-o` or `--output`: Optional: output file with active trackers
