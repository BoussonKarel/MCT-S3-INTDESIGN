# CSS Variables
## Wat

 - CSS Variables / Custom properties / Cascading variables
 - Veelgebruikte values naar variables
 - To keep consistency, set globial variables for everything except layout values

## Opbouw & syntax
**Defining the variable**
```css
:root {
	--my-cool-color: HotPink;
	--ITS-CASE-SENSITIVE: true;
	--its-case-sensitive: f
}
```

**Applying the variable**
```css
color: var(--my-cool-color);
```

## Cascade

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbODQyNjg4NDI4LC0xNzkxODcxMTMzLDk3MT
MwMTgzNSwxNDMzMzAxMDUsNzMwOTk4MTE2XX0=
-->