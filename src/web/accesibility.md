# ♿️ Accesibility

## Tools

- [Webhint](https://webhint.io/)
- [A11yproject](https://a11yproject.com/)
- [Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [a11ymatters](https://www.a11ymatters.com) - Let's care more about web accessibility

## Voice Over

| Action | Command |
| --- | --- |
| Start Voice Over | `Command`+`F5` |
| Voice Over Key  | `Control`+`Option` |
| Rotor (All the content of the page) : Open| `Control`+`Option`+`U` |
| Rotor (All the content of the page) : Navigation| ⬅ ➡ |
| Start Reading the page | `Control`+`Option`+`A` |


## Tips

### Display accesibility informations in **Chrome Browser**

`Cmd` + `Shift` + `P` => `show accessibility`

## Articles & Ressources

- [🎥 Headings, Landmarks and Tabs](https://youtu.be/HE2R86EZPMA)
- [🎥 Practical Tips For Building More Accessible Front-Ends at SmashingConf Feiburg 2019](https://vimeo.com/362155651)
- [Reading a Web Page using Apple Voice Over](https://medium.com/accessibility-a11y/reading-a-web-page-using-apple-voice-over-cd1a637e6285)
- [The web accessibility basics](https://medium.com/@MarcoZehe/the-web-accessibility-basics-bec77236949e)
- [Accessibility Statistics](https://www.interactiveaccessibility.com/accessibility-statistics)
- [Accessibility guidelines for UX Designers](https://uxdesign.cc/accessibility-guidelines-for-a-ux-designer-c3ba775539be)

## Guide lines

### Disabled

This isn’t an effective way to disable a form field because it only affects **pointer events**. Users can still interact with the element if navigating using a **keyboard**.


✅Do 

```html
<style>
    [disabled] { 
        cursor: not-allowed;
    }
</style>

<form>
    <button disabled>Submit</button>
</form>
```

🛑Don't

```html
<style>
    .disabled { 
        cursor: not-allowed;
        pointer-events: none;
    }
</style>

<form>
    <button class="disabled">Submit</button>
</form>
```

## 🙌 Contributors 

- Yann Duval
