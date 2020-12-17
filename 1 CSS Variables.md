# CSS Variables
## Wat

 - CSS Variables / Custom properties / Cascading variables
 - Veelgebruikte values naar variables
 - To keep consistency, set globial variables for everything except layout values

## Opbouw & syntax
- **Custom property: defining the variable**
```css
:root {
	--CASE-SENSITIVE: red;
	--case-sensitive: green;
}
```

- **Cascading variable: applying the variable**
```css
p {
	color: var(--CASE-SENSITIVE); /* red */
}

.foo {
	background-color: var(--case-sensitive); /* green */
}
```

- **Use calc() to do math**
```css
:root {
	--whitespace-lg: calc(var(--whitespace) * 2);
}
```

- **Kan bestaan uit andere variables**
- **en shorthand values bevatten**
```css
:root {
	--border-width: 1px;
	--border-type: solid;
	--border-color: blue;
	--border: var(--border-width) var(--border-type) var(--border-color);
}
```

- **Default values (with other variables)**
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
### Global scoped variables
**:root** is a CSS pseudo-class selector used to select the element that represents the root of the document

:root is hetzelfde als html, maar specifieker

Kan je overal hergebruiken **en** overschrijven.
 - colors
 - whitespace
 - border-radius
 - transitions
 - ...

### Local scoped variables
Local scoped variables worden gedeclareerd binnen een specifieke selector.

Ze hebben access tot global scoped variables.

Ideaal voor components.

```css
.alert {
	--alert-color: #222;
	color: var(--alert-color);
	border-color: var(--alert-color);
}

:root {
	--global-fontSize: 16px;
}

.c-button {
	--button-fontSize: var(--global-fontSize);
	font-size: var(--button-fontSize);
}
```

## Naming system
### The two-level theming system
Systeem om global variables te gebruiken in local variables

#### Global level
De hoofdreden om global variables te hebben is consistentie.

```css
--global-concept-modifier-state-propertyCamelCase
```
 - Concept: space, main-title, text...
 - State: hover, expanded...
 - Modifier: sm, lg...
 - propertyCamelCase: backgroundColor, fontSize...
 
```css
:root {
	/* --global-concept-size */
	--global-spacer-sm: .5rem;
	/* --global-concept-PropertyCamelCase */
	--global-main-title-FontSize: 2rem;
	--global-secondary-title-FontSize: 1.8rem;
	--global-body-FontSize: 1rem;
	/* --global-state-PropertyCamelCase */
	--global-hover-BackgroundColor: #ccc;
}
```

#### Local level
```css
--block__element-modifier-state-propertyCamelCase
```
 - The block__element-modifier the selector name is something like alert__actions or alert-primary
 - A state is something like hover or active
 - The value of component scoped variables is always defined by a global variable
```css
.c-alert {
	/* Component scoped variables are always defined by global variables */
	--c-alert--Padding: var(--global-spacer-md);
	--c-alert--primary--BackgroundColor: var(--global-primary-color);
	--c-alert__title--FontSize: var(--global-secondary-title-fontSize);
	/* --block--propertyCamelCase */
	padding: var(--c-alert-padding);
}

/* --block-state-propertyCamelCase */
.c-alert--primary {
	background-color: var(--c-alert-primary-backgroundColor);
}

/* --block__element-propertyCamelCase */
.c-alert__title {
	font-size: var(--c-alert__title-fontSize);
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNTQ4NjQyNDEsLTIxMzg4NzgxODAsMT
UyNDEyMDAzOSw0NDc3OTg5MzQsLTEwMTgwNjc1NDAsLTEwOTM2
MjcwODQsLTUxMTQ2MjY2Miw3OTI5MTMxMjQsMTI3Mzg1MjAxMy
wtODk1ODMxMzg2LC0xNzkxODcxMTMzLDk3MTMwMTgzNSwxNDMz
MzAxMDUsNzMwOTk4MTE2XX0=
-->