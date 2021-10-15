# plex-cli
SIMPLE CLI for streaming movies from a local plex server without opening a web browser. Useful for...IDK, but it's useful for my 2GB netbook

## Requirements

* `fuzzy-wuzzy` - (`pip install fuzzywuzzy`, optional `pip install python-Levenshtein`) used for fuzzy string matching to match search terms with library items
* `mpv` - (`apt install mpv`) used for playing media from the command line

## Installation
1. Put the Python script itself in your `PATH` somewhere
1. Fill in the configuration values at the top of the script:
  * `PLEX_ADDR`: the IP address of the server. Definitely works for local IP addresses, but I _think_ it works for the "external" IPs leased from Plex.
  * `PLEX_PORT`: the port the server's hosted on. Usually `32400` locally.
  * `PLEX_AUTH_TOKEN`: the value of the `X-Plex-Token` header - log in to the server in a web browser and snoop your traffic to grab this. AFAIK these tokens take a while to expire...
  * `PLEX_LIBRARY_ID`: the integer ID of the library the script should search. Currently this script only works for movies. Again, log in to the server in a web browser and snoop your traffic while you navigate to the library - you're looking for a request to `http://{plex-url}/library/sections/{PLEX_LIBRARY_ID}/...`.
1. Make sure your dependencies are installed - currently tested and working for `mpv-0.27.2`
1. Try it out: `plex --all` or `plex star wars`