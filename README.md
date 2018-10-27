# smol-ff

A `userChrome.css` based theme for Firefox that removes all the stuff I don't need and makes the UI take very little vertical space. My screen is only 768px tall!

This is only tested with latest FF Dev Edition, on Arch Linux, on a 1366×768 screen, with Firefox configured to the dark theme, with normal density, and without any of the spacer stuff that it has in the nav bar by default. I don't guarantee that it works _anywhere else whatsoever_.

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

## License

[CC-BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/) - Copy and edit this any way you like, but link back to here & use the same license.
