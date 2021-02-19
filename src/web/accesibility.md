# ♿️ Accesibility

## Tools

- [Webhint](https://webhint.io/)
- [A11yproject](https://a11yproject.com/)
- [Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [a11ymatters](https://www.a11ymatters.com) - Let's care more about web accessibility
- [Accessibility checklist used by Duet’s core team](https://www.duetds.com/accessibility/)
- [React Aria](https://react-spectrum.adobe.com/react-aria) - A library of React Hooks that provides accessible UI primitives for your design system.

## Chrome extentions

- [Axe](https://www.deque.com/axe/) - The Standard in Accessibility Testing

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
- [Scaling accessibility with a design system](https://gerireid.com/accessibility.html)

## Guide lines

### Disabled

Use `user-select: none` to disable. Don't use `pointer-events: none` because the users can still interact with the element if navigating using a **keyboard**.

✅Do 

```html
<style>
    [disabled] { 
        cursor: not-allowed;
        user-select: none;
    }
</style>

<form>
    <button disabled>Submit</button>
</form>
```

🛑Don't

```html
<style>
    [disabled], .disabled { 
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
- Gabriel Lebaudy
