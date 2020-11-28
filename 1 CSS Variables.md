# CSS Variables
## Wat

 - CSS Variables / Custom properties / Cascading variables
 - Veelgebruikte values naar variables
 - To keep consistency, set globial variables for everything except layout values

## Opbouw & syntax
**Defining the variable**
```css
:root {
	--ITS-CASE-SENSITIVE: red;
	--its-case-sensitive: green;
}
```

**Applying the variable**
```css
p {
	color: var(--ITS-CASE-SENSITIVE); /* red */
}
```

**Use calc() to do math**
```css
:root {
	--whitespace-lg: calc(var(--whitespace) * 2);
}
```

**Kan bestaan uit andere variables**
```css
:root {
	--border-width: 1px;
	--border-type: solid;
	--border-color: blue;
	--border: var(--border-width) var(--border-type) var(--border-color);
}
```

**Default values (with other variables)**
```css
.c-button {
	border: 1px solid var(--button-color, HotPink);
	/* border: 1px solid var(--button-color, var(--text-color)); */
}

.c-button--beta {
--button-color: red;
}
```

## Cascade
**Alle elementen binnen de root waar je --my-cool-color toepast, zullen HotPink overerven.**
```css
:root {
--my-cool-color: HotPink;
}
```
**Alle elementen in .foo ervan #BADA55 over.**
```css
p {
color: var(--my-cool-color);
}
.foo {
--my-cool-color: #BADA55;
}
```

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTg5NTgzMTM4NiwtMTc5MTg3MTEzMyw5Nz
EzMDE4MzUsMTQzMzMwMTA1LDczMDk5ODExNl19
-->