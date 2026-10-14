# Valley Overlay updates

Valley Overlay (2.5.1 and newer) checks `latest.json` here for new versions and
downloads the `.valley-update` file it names. Each file is signed; the overlay
checks its size, checksum and signature before installing.

To publish: run `node make-update.js <key.pem> dist` in the overlay source and
commit `dist/latest.json` plus the new `.valley-update` file here. Older update
files can be deleted. Never commit the signing key.
