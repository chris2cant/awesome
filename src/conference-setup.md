# Conference Setup

## Setup

- Microphone
  - [Blue Yeti](https://www.bluemic.com/en-us/products/yeti/)
- Camera
  - [Epocam Pro](https://www.elgato.com/en/epoccam)

## Use for calls

- [OBS]()

## Microsoft Teams

### Enable virtual camera

[Source](https://answers.microsoft.com/en-us/msteams/forum/msteams_tfb-msteams_tfmac/microsoft-teams-mac-os-client-is-not-recognizing/d9e863be-d9a4-4d03-a4b8-1b5c7df58828) - Microsoft Teams Mac OS client is not recognizing external cameras after updating to version 1.3.00.18164.
```
xcode-select --install (only if you haven't already)
sudo codesign --remove-signature "/Applications/Microsoft Teams.app"
sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper.app"
sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (GPU).app"
sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Plugin).app"
sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Renderer).app"
```
