 # VSCode

- editor.formatOnSave : `true`
- files.autoSave : `onFocusChange`
- editor.tabSize : `2`
- git.inputValidationSubjectLength: `100`

## Prettier - Code formatter

- prettier.singleQuote : `true`
- prettier.tabWidth : `2`
- prettier.tslintIntegration : `true`
- prettier.stylelintIntegration: `true`

## Plugins

- [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2)
- TSLint
- Sass
- Stylelint
- [es6-string-html](https://marketplace.visualstudio.com/items?itemName=Tobermory.es6-string-html) (Syntax highlighting in es6 multiline strings)
- [Angular2-switcher](https://marketplace.visualstudio.com/items?itemName=infinity1207.angular2-switcher)
- [Turbo Console log](https://marketplace.visualstudio.com/items?itemName=ChakrounAnas.turbo-console-log)
- [VSCode HackerTyper](https://marketplace.visualstudio.com/items?itemName=jevakallio.vscode-hacker-typer)
- [Jenkinsfile support](https://marketplace.visualstudio.com/items?itemName=secanis.jenkinsfile-support)
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- [Typescript Hero](https://marketplace.visualstudio.com/items?itemName=rbbit.typescript-hero)
- [SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)
- [Draw.io](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)

### Theme

- Material Icon Theme
- Material Theme

## Snippets

### Console warn a variable

```json
{
	"Print value": {
		"scope": "javascript,typescript",
		"prefix": "cwv",
		"body": [
			"console.warn('[$1]', $1);"    
		],
		"description": "Print value"
	}
}
```
 
## VS Code Settings

[settings.json](https://gist.github.com/chris2cant/e84a26a570932014711eed459353bbc3) (Christophe de Canteloube)

## Personal choice

- workbench.editor.showTabs: `false` (Warning : Disable tabs navigation)
- explorer.autoReveal: `false` (Disable explorer autoscroll to source on file focus)
