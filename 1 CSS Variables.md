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
**CSS Variables zijn onderhevig aan de cascade en inheritance regels**
Alle elementen binnen de root waar je --my-cool-color toepast, zullen HotPink overerven.
```css
:root {
--my-cool-color: HotPink;
}
```
Alle elementen in .foo ervan #BADA55 over.
```css
p {
color: var(--my-cool-color);
}
.foo {
--my-cool-color: #BADA55;
}
```
**CSS Variables kunnen conditioneel zijn met @media en andere conditionele regels**

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbOTE5ODUwNzE4LC04OTU4MzEzODYsLTE3OT
E4NzExMzMsOTcxMzAxODM1LDE0MzMzMDEwNSw3MzA5OTgxMTZd
fQ==
-->