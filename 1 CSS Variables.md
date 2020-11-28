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
	--border-width: 1;
	--border-type: .1s;
	--border-color: ease-out;
	--transition: var(--transtion-property) var(--transition-duration) var(--transition-timingfunction);
}
```

**Default values**
```css
.c-button {
	border: 1px solid var(--button-color, HotPink);
}

.c-button--beta {
--button-color: red;
}
```

## Cascade

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzU0NDY3ODksLTE3OTE4NzExMzMsOT
cxMzAxODM1LDE0MzMzMDEwNSw3MzA5OTgxMTZdfQ==
-->