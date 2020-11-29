# Focus on forms
## Form
- HTML forms are a very powerful tool for interacting with users
- Groot deel van een digitale interface
- In veel vormen en maten
### Basic form syntax
```html
<form action=“”>
	<input type=“”>
	...
	Submit
</form>
```
**Maak geen forms zonder (submit) button!**
Zonder (submit) button kan je niet op Enter duwen

## Input types
Belangrijkste, te kennen types:
- Text-achtigen
- Time-achtigen
- Option-achtigen
- Textarea
- Select
- Range
- Hors catégorie
### HTML5 Input types
- Browser validatie
- Smartphone keyboard verandert (letters naar nummers...)

### Text-achtigen
Zien er visueel ongeveer hetzelde uit.
- **text:** basis input type voor HTML5 input types
- **password:** vervangt letters door bolletjes
- **email:** valideert de browser enkel als je een correct e-mailadres invult
- **number:**
- - aanvaardt enkel nummers
- - heeft pijltjes om te vermeerderen of verminderen
- **tel:** aanvaardt ook enkel nummers

### Time-achtigen
Zien er visueel ongeveer hetzelfde uit als de text-achtigen
- **date:** toont een native date picker
- **week:** toont een variant van de native date picker
- **month:** toont een variant van de native date picker
- **number:** aanvaardt enkel nummers
- **tel:** handig voor mobile

### Option-achtigen
**checkbox**
 - Meerdere keuzes mogelijk uit een aantal keuzes
 - Of kan alleen bestaan

**radio (button)**
 - Slechts 1 keuze mogelijk uit een aantal keuzes
 - Kan niet alleen bestaan, altijd in een group
 - Gekoppeld aan elkaar door het name attribuut
 - Niet voor enkele binaire keuzes

### Checkbox or toggle
|Checkbox|Toggle|
|--|--|
|Checked of niet|Aan of Uit|
|Confirmatie nodig|Instant response zonder confirmatie|
|Opties die bij elkaar horen|Afzonderlijke features of settings|
|Checken van sub-options (intermediate state)|
|Enkele ja/nee optie|Enkele aan/uit beslissig

![Intermediate state](https://i.imgur.com/1I29nDy.png)

**Checkbox**
- Contextual state
- Heeft invloed op het huidige scherm
- Opposing options

**Toggle switch = veredelde checkbox**
- System state
- Invloed op de volledige app
- Binary options

![Contextual State or System State](https://i.imgur.com/xJro1eE.png)

### Textarea
```html
<textarea></textarea>
```
- Geen input type
- Apart element
- multi-line text input control

### Select
```html
<select>
	<option value="volvo">Volvo</option>
	<option value="mercedes">Mercedes</option>
</select>
```
- Geen input type
- Apart element
- drop-down list
- Option tags define the available options in the list
- Native select behouden als je designt: gebruiksvriendelijker op smartphone

### Range
- Slider control
- Voor nummers
- Default range 0 - 100
- Restrictions mogelijk met min, max, step attributen

### Hors catégorie
- **file:** file upload
- **hidden:** voor developers
- **color:** toont vreemde color picker

## Attributes

## Labels

## Button

## Focus

## Validation

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1NDAwNDAyNSwtODcxNzU1NDM0LDU3Nj
g5OTcwNywtMTExODY3NDk0NiwtMTEyMjkyMjQ3OCwxNzAwMjYw
MzMzLC03MjA5NjczOTgsLTU4ODA4NjAsLTIwODg3NDY2MTJdfQ
==
-->