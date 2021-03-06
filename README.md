<p align="center">
<img src="https://cloud.githubusercontent.com/assets/7145349/16916971/6bd3343a-4cb4-11e6-86cc-e3bc9399a9b0.png">
</p>

# PokemonGo Map

[![Build Status](https://travis-ci.org/AHAAAAAAA/PokemonGo-Map.svg?branch=master)](https://travis-ci.org/AHAAAAAAA/PokemonGo-Map)  [![Coverage Status](https://coveralls.io/repos/github/AHAAAAAAA/PokemonGo-Map/badge.svg?branch=master)](https://coveralls.io/github/AHAAAAAAA/PokemonGo-Map?branch=master)

Live visualization of all the pokemon (with option to show gyms and pokestops) in your area. This is a proof of concept that we can load all the pokemon visible nearby given a location. Currently runs on a Flask server displaying a Google Maps with markers on it.

Building off [Mila432](https://github.com/Mila432/Pokemon_Go_API)'s PokemonGo API, [tejado's additions](https://github.com/tejado/pokemongo-api-demo), [leegao's additions](https://github.com/leegao/pokemongo-api-demo/tree/simulation) and [Flask-GoogleMaps](https://github.com/rochacbruno/Flask-GoogleMaps).

For general support, join [our discord server](https://discordapp.com/invite/qbpVH6b).

# Installation
`pip install -r requirements.txt`

# Usage
`python example.py -a authService -u myUsername -p myPassword -l "Boulder, CO" -st 5`

| Flag | Description                             |
|------|-----------------------------------------|
| -a   | Auth Service (ptc or google)            |
| -u   | Username                                |
| -p   | Password                                |
| -l   | Any location Google Maps can understand |
| -st  | Steps to take                           |
| -i, --ignore | Comma-separated list of Pokémon to ignore |
| -o, --only   | Comma-separated list of Pokemon to search for exclusively |
| -dp, --display-pokestop | Display pokestop                   |
| -dg, --display-gym  | Display gym                   |
| -H, --host  | Set web server listening host    |
| -P, --port  | Set web server listening port    |

Note:
5 steps is approximately a 1.2km radius. More than 10 is redundant (you usually can't walk that far before despawn anyway)

# FAQ

`Exception, e <-`
`Invalid syntax.`
* You are using python 3, download python 2.7 instead.

`pip or python is not recognized as an internal or external command`

* replace pip with C:\Python27\Scripts\pip
* replace python with C:\Python27\python

* Can I sign in with Google? Not yet, we're working on it, until then get a Trainer Club account

* I'm on Windows, why does nothing work? See if anything in https://www.reddit.com/r/pokemongodev/comments/4t80df/wip_pokemon_go_map_visualization_google_maps_view/d5feu2f helps
