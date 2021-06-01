# Design System - States

## Descriptions

|State|CSS|Description|Example|
|---|---|---|---|
|Default||Default state||
|Hover|:hover|When a user has placed a cursor above an interactive element||
|Disabled|:disabled|User interaction disabled|Button, Input|
|Focus|:focus|When a user has highlighted an element (Keyboard or Voiceover)||
|Active|:active|When you currently click on it (During Mouse down) |Button|
|Selected|:selected|A user choice|Menu|
|Checked|:checked|On statement. A user option|Checkbox, Radio, Switch|
|Not Checked|:not(:checked)| Off statement. A user option|Checkbox, Radio, Switch|
|Visited|:visited|Link already visited||
|Invalid|:invalid|Error field||
|Read Only|:read-only|On readable not writable|Input|

|Component|Default|Hover|Disabled|Focus|Active|Selected|Checked / Not Checked|Visited|Valid / Invalid|Read Only|
|---|---|---|---|---|---|---|---|---|---|---|
|Button|✅|✅|✅|✅|✅|||✅|||
|Input Text Field|✅|✅|✅|✅|||||✅|✅|

## Components

## Button

- Default
- Hover
- Disabled
- Focus
- Active
- Visited

## Input text field

- Default
- Not empty
- Hover
- Disabled
- Focus
- Read Only
- Invalid
  - Invalid + Default
  - Invalid + Hover   
  - Invalid + Focus
  - Invalid + Disabled
- Warning
  - Warning + Default
  - Warning + Hover   
  - Warning + Focus
  - Warning + Disabled
- Valid
  - Valid + Default
  - Valid + Hover   
  - Valid + Focus
  - Valid + Disabled
- Required
- Label

## Switch

- Default
- Disabled
- Checked / On
- Not checked / Off
- Checked + Active
- Not checked + Active
- Animation between Checked/Not Checked

## Ressources

- [Design Encyclopedia](https://www.designencyclopedia.io/)
- [Checklist Design](https://www.checklist.design/)
- [AntDesign - Figma](https://www.figma.com/file/9UVJgFX0L3mez1fMzsIp7J/(Preview)-Ant-Design-System-for-Figma-2.0-(Light-Theme)?node-id=371%3A8955)
