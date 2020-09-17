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

- [Angular2-switcher](https://marketplace.visualstudio.com/items?itemName=infinity1207.angular2-switcher)
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2)
- [Codemetrics](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics)
- [CSS Flexbox Cheatsheet](https://marketplace.visualstudio.com/items?itemName=dzhavat.css-flexbox-cheatsheet)
- [es6-string-html](https://marketplace.visualstudio.com/items?itemName=Tobermory.es6-string-html) (Syntax highlighting in es6 multiline strings)
- [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - Current Line Blame
- [Gitmoji](https://marketplace.visualstudio.com/items?itemName=Vtrois.gitmoji-vscode) - Emoji for commit message
- [Jenkinsfile support](https://marketplace.visualstudio.com/items?itemName=secanis.jenkinsfile-support)
- [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock) - Workspace color for multiple window
- [SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)
- [Turbo Console log](https://marketplace.visualstudio.com/items?itemName=ChakrounAnas.turbo-console-log)
- [Typescript Hero](https://marketplace.visualstudio.com/items?itemName=rbbit.typescript-hero)
- [VSCode HackerTyper](https://marketplace.visualstudio.com/items?itemName=jevakallio.vscode-hacker-typer)
- Sass
- Stylelint
- TSLint
- Schema
	- [Draw.io](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
	- [Sequence Diagrams](https://marketplace.visualstudio.com/items?itemName=AleksandarDev.vscode-sequence-diagrams)

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
