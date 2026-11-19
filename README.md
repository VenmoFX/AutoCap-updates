# AutoCap updates

AutoCap (Premiere Pro plugin) reads `version.json` from this repo when the panel opens.
If the version here is higher than the installed one, the panel shows an update notice with a Download button.

## How to release an update

1. Build the new plugin and set the same version number inside it (`APP_VERSION` in `js/main.js`, and the version in `CSXS/manifest.xml`).
2. In Payhip, open the AutoCap product and replace `AutoCap_v1.0.zip` with the new zip.
3. Edit `version.json` in this repo:
   - `version`: the new number, for example `1.1.0`
   - `notes`: one short line about what is new
   - `url`: leave it as it is
4. Commit. Everyone with an older version sees the notice the next time they open the panel.

Only this file lives here. The plugin itself is never uploaded to GitHub.
