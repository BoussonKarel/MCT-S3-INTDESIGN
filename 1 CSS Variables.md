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

**Kan meerdere variables bevatten**

**en kan shorthand values bevatten**
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
**CSS Variables Are Subject to the Cascade and Inheritance rules**
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
**CSS Variables can be made conditional with @media and other conditional rules**
```css
@media screen and (min-width: 768px) {
	:root {
		--whitespace: 2em;
	}
}
```
**Ideal for dark themes**
```css
:root {
	--color: white;
	--background-color: black
}

@media (prefers-color-scheme: dark) {
	:root {
		--color: black;
		--background-color: white
	}
}
```

## Hoisting
**Accessing a Variable First and Declaring Later**
```css
body{
	background: var(--bg-fill);
}

:root{
	--bg-fill: green;
}
```

## Global vs local scope
:root is a CSS pseudo-class selector used to select the element that represents the root of the document

:root is hetzelfde als html, maar specifieker

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA4ODM5MTA1LC01MTE0NjI2NjIsNzkyOT
EzMTI0LDEyNzM4NTIwMTMsLTg5NTgzMTM4NiwtMTc5MTg3MTEz
Myw5NzEzMDE4MzUsMTQzMzMwMTA1LDczMDk5ODExNl19
-->