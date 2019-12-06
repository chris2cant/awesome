# Angular - Storybook Guide

## Install

### Install via npm

```sh
npm install --save-dev @storybook/angular babel-loader @babel/core
```

### Add npm script

./package.json
```json
{
  ...
  "scripts": {
    "storybook": "start-storybook"
  }
}
```

### Create config files

Execute this command a the root folder

```sh
mkdir .storybook; cd .storybook; touch addons.js; touch config.js; touch tsconfig.json; touch preview-head.html; cd -
```

#### config.js


./.storybook/config.js
```js
import { configure, addParameters } from '@storybook/angular';

addParameters({
  options: {}
});

// Loading stories dynamically
const req = require.context('..', true, /\.story\.ts$/);

// Index page
require('../stories/index.story.ts');

function loadStories() {
  req.keys().forEach(filename => req(filename));
}

configure(loadStories, module);
````

### tsconfig.json

./.storybook/tsconfig.json
```json
{
  "extends": "../tsconfig.json",
  "exclude": [
    "../src/test.ts",
    "../src/**/*.spec.ts",
    "../projects/**/*.spec.ts"
  ],
  "include": ["../src/**/*"]
}
```

### Create stories folder

Execute this command a the root folder

```sh
mkdir stories; cd stories; touch index.story.ts; cd -
```

### Index story

./stories/index.story.ts
```js
import { storiesOf, moduleMetadata } from '@storybook/angular';

const modules = {
  imports: [],
  declarations: []
};


storiesOf('Storybook', module)
  .addDecorator(moduleMetadata(modules))
  .add('Welcome !', () => ({
    template: `
    	<div>
    		Welcome
    	</div>
    `
  }));

```

### It's working !

```sh
# Default run
npm run storybook
# Run with defined port
npm run storybook -- --port 4242
```

## Addons 

```sh
# @storybook/addons : Addons available
# @storybook/addon-actions : Display data received by event handlers
# @storybook/addon-knobs : Dynamic props
# @storybook/addon-viewport : Mobile display
npm install --save-dev @storybook/addons @storybook/addon-actions @storybook/addon-knobs @storybook/addon-viewport
```

`./.storybook/addons.js`

```js
// The order decide the order in storybook tab
import '@storybook/addon-knobs/register';
import '@storybook/addon-actions/register';
import '@storybook/addon-viewport/register';
```
