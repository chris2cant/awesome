# Mac

- [Plash](https://apps.apple.com/fr/app/plash/id1494023538?mt=12) - Make any website your desktop wallpaper.

## Shortcuts

|Shortcut|Description|
|---|---|
|Screen shot on clipboard|`Ctrl`+`⌥`+`Maj`+`4`|
|Switch windows inside same space|`Ctrl`+`F4` (You can customise to `⌥` `⇥`)|

## App

- [Lunar](https://lunar.fyi) - Intelligent adaptive brightness for your external display
- [Spectacle App](https://www.spectacleapp.com) - Move and resize windows with ease (Free)
- [Rectangle](https://github.com/rxhanson/Rectangle) - Window management app based on Spectacle, written in Swift.
- [F.Lux](https://justgetflux.com/) - Adapt screen color to reduce eye strain (Free)
- [ImageOptim](https://imageoptim.com/fr) - Image optimizer (Free)

## Custom defaults

### Autohide dock time

```sh
// 0.2 seconds
defaults write com.apple.dock autohide-time-modifier -float 0.2; killall Dock;
// Restore defaults
defaults delete com.apple.dock autohide-time-modifier; killall Dock;
```

## 📰 Articles

- [How to Set Up Your MacBook for Web Development in 2020](https://link.medium.com/KpPitCwXE9)

## Accessories

- [Twelve South](https://www.twelvesouth.com)

## 🙌 Contributors

- Jean-Christophe Queval-Bourgeois
