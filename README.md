# smol-ff

A `userChrome.css` based theme for Firefox that removes all the stuff I don't need and makes the UI take very little vertical space. My screen is only 768px tall!

This is only tested with latest FF Dev Edition, on Arch Linux, on a 1366×768 screen, with Firefox configured to the dark theme, with normal density, the menu bar set to auto-hide, and without any of the spacer stuff that it has in the nav bar by default. I don't guarantee that it works _anywhere else whatsoever_.

![](./screenshot.png)

## Features

 - Tab line and navbar are on a single line
 - Simple small monospace font and small unfancy tabs
 - Settings menu is on the far right
 - Compact SSL info, certificate owner name hidden when focusing the URL bar to make space
 - Menu bar shows on top of the tab/nav bar when pressing Alt
 - Buttons with easy keyboard shortcuts removed:
   - reload (ctrl R),
   - new tab (ctrl T),
   - home (ctrl W then ctrl T),
   - history (ctrl H)
 - Buttons I've never used removed:
   - some crash reporting thing,
   - pocket

Ideally, extension icons would be shown to the right of the tab bar, but the way the chrome DOM is laid out makes that very brittle. I opted for the simpler implementation here and recommend hiding most of the extension icons instead (right-click » pin to overflow menu).

## Install

Put the `profile/chrome/userChrome.css` file in your FF profile.

```bash
cd ~/.mozilla/firefox/*.dev-edition-default<TAB>
mkdir -p chrome
cd chrome
curl -O https://raw.githubusercontent.com/goto-bus-stop/smol-ff/default/profile/chrome/userChrome.css
```

Then restart the browser.

## Uninstall

```bash
cd ~/.mozilla/firefox/*.dev-edition-default<TAB>
rm chrome/userChrome.css
```

## Developing

All files in `profile` are gitignored by default. You can work on the theme by doing:

```bash
firefox-developer-edition --new-instance --profile ./profile
```

Then see the "Live-Testing styles" section here for further instructions: https://reddit.com/73dvty

## License

[CC-BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/) - Copy and edit this any way you like, but link back to here & use the same license.
