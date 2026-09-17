# Zen Browser Custom UI

My personal **userChrome.css** setup for Zen Browser, split into small modules so
each tweak can be found, fixed, or disabled on its own.

## Install

1. `about:support` → Profile Folder → **Open Folder**
2. Create a `chrome/` folder if it doesn't exist
3. Copy `userChrome.css` and the `modules/` folder into `chrome/`
4. In `about:config`, set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
   (skip if you already run userChrome.css)
5. Restart Zen

`userChrome.css` is only the entry point — everything lives in a module:

```css
@import url("modules/toolbar.css");
@import url("modules/urlbar.css");
@import url("modules/sidebar.css");
@import url("modules/compact-mode.css");
@import url("modules/split-view.css");
@import url("modules/findbar.css");
@import url("modules/menus.css");
@import url("modules/minplayer.css");
@import url("modules/picture-in-picture.css");
@import url("modules/glance.css");
```

## Modules

| Module | What it does |
| --- | --- |
| `toolbar.css` | Essentials spacing, minplayer button order, main-menu button logo |
| `urlbar.css` | URL bar icon order, centered text, hides the extension label, native bookmark star |
| `sidebar.css` | Floating bookmark/history sidebar |
| `compact-mode.css` | Slimmer compact sidebar + hide-tabbar sizing |
| `split-view.css` | Auto-hiding split-view separator |
| `findbar.css` | Floating find bar |
| `menus.css` | Unified menu (site data header) tweaks |
| `minplayer.css` | Minplayer layout, hover expansion, playing glow |
| `picture-in-picture.css` | Arc-style PiP window (controls, scrubber, settings) |
| `glance.css` | Glance buttons on the opposite side |

Preview images/GIFs live in [`assets/`](assets).

## Notes

- Made and tested on Zen Browser.
- Feel free to edit or build on top of it — it's meant to be flexible :)
