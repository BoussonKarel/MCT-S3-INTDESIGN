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

## Cascade

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3NTgzNDc2NzAsLTE3OTE4NzExMzMsOT
cxMzAxODM1LDE0MzMzMDEwNSw3MzA5OTgxMTZdfQ==
-->