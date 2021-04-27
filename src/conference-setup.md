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

## OBS

### Filters

- [OBS NDI](https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/)
- [NDI HX Tools](https://www.newtek.com/ndihx/products/)
- [TDR VOS SlickEQ](https://www.tokyodawn.net/tdr-vos-slickeq/)
- [TDR Nova](https://www.tokyodawn.net/tdr-nova/)
- [TDR Kotelnikov](https://www.tokyodawn.net/tdr-kotelnikov)
- [Wider](https://polyversemusic.com/products/wider)
- [Auburn sounds Graillon](https://www.auburnsounds.com/products/Graillon.html)
- [TAL Reverb 4](https://tal-software.com/products/tal-reverb-4)

#### TDR VOS SlickEQ (Free)

My preset

```xml
<TDRVOSSlickEQ _preset_name="Christophe de Canteloube" lowBandGainParam="7.5" lowBandFreqParam="85" lowBandShapeParam="Bell" midBandGainParam="-4.5" midBandFreqParam="400" highBandGainParam="9.0" highBandFreqParam="5000" highBandShapeParam="Shelf" eqModelParam="German" eqSatParam="On" hpFreqParam="50" outSatModelParam="Deep" outSatDriveParam="9.0" outGainParam="6.0" bypassParam="Off" modeParam="Stereo" lowBandBypassParam="Off" midBandBypassParam="Off" highBandBypassParam="Off" autoGainParam="Off" qualityParam="Live"/>
```

#### TDR Nova (Free)

My preset

```xml
<TDRNova _preset_name="Christophe de Canteloube" bandSelected_1="Off" bandActive_1="On" bandGain_1="0.0" bandQ_1="0.50" bandFreq_1="100" bandType_1="Bell" bandDynActive_1="On" bandDynThreshold_1="-12.0" bandDynRatio_1="10.2" bandDynSplit_1="On" bandDynAttack_1="20" bandDynRelease_1="200" bandSelected_2="Off" bandActive_2="Off" bandGain_2="0.0" bandQ_2="0.60" bandFreq_2="400" bandType_2="Bell" bandDynActive_2="Off" bandDynThreshold_2="0.0" bandDynRatio_2="2.0" bandDynSplit_2="On" bandDynAttack_2="10" bandDynRelease_2="180" bandSelected_3="Off" bandActive_3="Off" bandGain_3="0.0" bandQ_3="0.50" bandFreq_3="2200" bandType_3="Bell" bandDynActive_3="Off" bandDynThreshold_3="0.0" bandDynRatio_3="2.0" bandDynSplit_3="On" bandDynAttack_3="5.0" bandDynRelease_3="160" bandSelected_4="On" bandActive_4="On" bandGain_4="0.0" bandQ_4="1.50" bandFreq_4="4200" bandType_4="Bell" bandDynActive_4="On" bandDynThreshold_4="-25.7" bandDynRatio_4="2.5" bandDynSplit_4="On" bandDynAttack_4="10" bandDynRelease_4="150" hpSelected_master="Off" hpActive_master="Off" hpFreq_master="15" hpType_master="24dB/oct" lpSelected_master="Off" lpActive_master="Off" lpFreq_master="30000" lpType_master="24dB/oct" bandGain_wide="0.0" bandDynActive_wide="Off" bandDynThreshold_wide="0.0" bandDynRatio_wide="1.5" bandDynAttack_wide="8.0" bandDynRelease_wide="200" bypass_master="Off" delta_master="Off" dryMix_master="0.0" gain_master="0.0" eqAutoGainParam="On" qualityParam="Eco" channelsParam="Stereo" analyzerModeParam="Analyzer: In" displayEqRangeParam="-/+ 12 dB" displayFFTRangeParam="48 dB" sidechainModeParam="Int SC" analyzerSpeedParam="Normal"/>
```

#### TDR Kotelnikov (Free)

My preset

```xml
<TDRKotelnikov _preset_name="Christophe de Canteloube" thresholdParam="-25.0" peakCrestParam="RMS" softKneeParam="9.0" ratioParam="2.5" attackParam="8.0" releasePeakParam="80" releaseRMSParam="250" makeUpParam="0.0" dryMixParam="off" dryWetParam="0.0" dryMixModeParam="Dry Mix" outGainParam="3.0" keyHPFrequencyParam="100" keyHPSlopeParam="6dB/Oct" keyStereoDiffParam="80" deltaParam="Off" bypassParam="Off" qualityParam="Eco" modeParam="Stereo" grDispScaleParam="3" grDispModeParam="Gain Reduction"/>
```

#### Expander (Default)

My Preset

![Capture d’écran 2021-04-09 à 11 03 59](https://user-images.githubusercontent.com/11084022/114156849-4c6c4080-9923-11eb-80e2-c423ecc1d5fb.png)
