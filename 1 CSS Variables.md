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
	--whitespace-lg: calc(var(--whitesp
}
```

## Cascade

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI5NzQ3Nzg4NywtMTc5MTg3MTEzMyw5Nz
EzMDE4MzUsMTQzMzMwMTA1LDczMDk5ODExNl19
-->