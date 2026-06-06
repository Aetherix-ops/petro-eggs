# Pterodactyl Egg Collection (Updated)

A collection of updated Pterodactyl Panel eggs with the latest runtime versions.
Forked and updated from pelican-eggs/eggs (https://github.com/pelican-eggs/eggs).

---

## Egg List

Runtime   | Version                        | File
----------|--------------------------------|------------------------------------------
Node.js   | 18 / 20 / 21 / 22 / 23 / 24 / 26 | nodejs/egg-node-js-updated.json
Python    | 3.10 / 3.11 / 3.12 / 3.13     | python/egg-python-generic.json
Bun       | 1.3 (Latest)                   | bun/egg-bun-generic.json
Deno      | 2.7 (Latest)                   | deno/egg-deno-generic.json

---

## Installation

1. Download the .json file for the runtime you need.
2. Open your Pterodactyl Admin Panel.
3. Go to Nests, then select or create a nest.
4. Click Import Egg and upload the .json file.
5. Create a new server using the imported egg.

---

## What Changed from the Original

Node.js
- Added Node.js 26.x support
- Fixed install script: replaced deprecated python with python3
- Added UNNODE_PACKAGES variable to uninstall packages

Python
- Added Python 3.13 support
- Fixed install script to use python3 and python3-pip

Bun
- Bun 1.3 - all-in-one runtime, bundler, and package manager
- Native TypeScript support without any configuration
- Support for extra packages via BUN_PACKAGES variable

Deno
- Deno 2.7 - security-first runtime with full npm compatibility
- Auto-caches dependencies from deno.json on install

---

## Variables (All Eggs)

Variable        | Description                          | Default
----------------|--------------------------------------|----------
MAIN_FILE       | Main file to run                     | index.js
AUTO_UPDATE     | Pull latest git on startup (1 = on)  | 0
GIT_ADDRESS     | Git repo URL                         | (empty)
BRANCH          | Git branch                           | master
USERNAME        | Git username for private repos       | (empty)
ACCESS_TOKEN    | Git token for private repos          | (empty)
USER_UPLOAD     | Skip git, use uploaded files (1 = on)| 0

---

## File Structure

    ptero-eggs/
    |- nodejs/
    |   |- egg-node-js-updated.json
    |- python/
    |   |- egg-python-generic.json
    |- bun/
    |   |- egg-bun-generic.json
    |- deno/
    |   |- egg-deno-generic.json
    |- README.md

---

## Changelog

v1.1.0 - 2026-06-06
- Added Bun 1.3 egg
- Added Deno 2.7 egg
- Added Python 3.13 egg
- Added Node.js 26 egg

v1.0.0
- Initial fork from pelican-eggs/eggs

---

## Note on Docker Images

Some images (especially Node.js 26) may not yet be published by parkervcp.
If unavailable, use the previous version as a fallback.
Track image availability at: https://github.com/parkervcp/yolks

---

## Contributing

Pull requests are welcome. If an egg is outdated or you want to add a new runtime:

1. Fork this repo.
2. Create a branch: git checkout -b add/runtime-name
3. Commit: git commit -m "add: egg for X runtime vY"
4. Open a Pull Request.

---

## License

MIT - Based on original work by pelican-eggs (https://github.com/pelican-eggs).
