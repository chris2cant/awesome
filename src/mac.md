# Mac

- [Plash](https://apps.apple.com/fr/app/plash/id1494023538?mt=12) - Make any website your desktop wallpaper.

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

## 🙌 Contributors

- Jean-Christophe Queval-Bourgeois
