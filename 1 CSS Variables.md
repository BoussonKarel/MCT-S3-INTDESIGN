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
	--transition-property: all;
	--transition-duration: .1s;
	--transition-timing-function: ease-out;
	--transition: var(--transtion-property) var(--transition-duration) var(--transition-timingfunction);
}
```

## Cascade

## Hoisting

## Global vs local scope

## Naming system

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjUwNzYyMzkxLC0xNzkxODcxMTMzLDk3MT
MwMTgzNSwxNDMzMzAxMDUsNzMwOTk4MTE2XX0=
-->