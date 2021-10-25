# plex-cli
SIMPLE CLI for streaming movies from a local plex server without opening a web browser. Useful for...IDK, but it's useful for my 2GB netbook

## Requirements

* `fuzzy-wuzzy` - (`pip install fuzzywuzzy`, optional `pip install python-Levenshtein`) used for fuzzy string matching to match search terms with library items
* `mpv` - (`apt install mpv`) used for playing media from the command line

## Installation
1. Put the Python script itself in your `PATH` somewhere
1. Make sure your dependencies are installed - currently tested and working for `mpv-0.27.2`
1. `cp plex.conf ~/.plex_conf`
1. Fill in the appropriate values in `~/.plex_conf`
1. Try it out: `plex --all` or `plex star wars`
