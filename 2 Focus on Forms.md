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
  - aanvaardt enkel nummers
  - heeft pijltjes om te vermeerderen of verminderen
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
Eigenschappen van de input
- type, value, id, name...

### Minimum attributes
- **type:** definieert het type input
- **name:**
  - voor developers
  - zorgt ervoor dat je weet wat je waar ingevuld hebt
  - (en om radio buttons aan elkaar te koppelen)
  - **Altijd een name voorzien!**

### Veelgebruikte attributes
- **value:**
  - Kan je gebruiken om een default value in te geven
  - Indien leeg wordt dit wat je hebt ingevuld
- **placeholder:**
  - hint
  - voorbeeld van wat de value moet zijn
  - verdwijnt automatisch als je begint te typen
  - **Placeholder nooit gebruiken als alternatief voor een label!**

### Lege attributes
- Hebben geen value
- Zijn waar of onwaar
- CSS pseudo classes
- Veel gebruikt
  - **Checked:** radio options & checkboxes
  - **Required:** browservalidatie
  - **Disabled:** kan je niet aanpassen en wordt ook niet gesubmit
  - **Readonly:** kan je niet aanpassen maar wordt wel gesubmit
  - **Autofocus:** focust automatisch op het input type

## Labels
- Gekoppeld aan een input
- Usability improvement: toggles the input
- **Elke input moet een label hebben!**
- **Niet vervangen door een placeholder!**
  - In een lang ingevuld formulier weet je op en duur niet meer wat je waar moet invullen
  - Alternatief: floating label

```html
<!-- Manier 1: apart aanspreekbaar-->
<label for=“input_id”>label text</label>
<input type=“text” name=“whatever” id=“input_id”>

<!-- Manier 2: label text niet aanspreekbaar met CSS -->
<label>
label text
<input type=“text” name=“whatever” id=“input_id”>
</label>
```

## Button
**Elk formulier moet een button hebben**
```html
<!-- Als input type -->
<input type=“submit” value=“verzenden”>
<input type=“button” value=“verzenden”>

<!-- Als button element -->
<button>verzenden</button>
```
**Gebruik het button element!**
```html
<button class=“c-button”>
	<span class=“c-button__label”>Verzenden</span>
	<svg class=“c-button__symbol>…</svg>
</button>
```
### States
- :hover
- :active
- focus

Deze volgorde in de CSS is belangrijk!

## Focus

## Validation

<!--stackedit_data:
eyJoaXN0b3J5IjpbOTQyMDkxMjEyLDEwMzU4Mjc1ODIsMTE1ND
AwNDAyNSwtODcxNzU1NDM0LDU3Njg5OTcwNywtMTExODY3NDk0
NiwtMTEyMjkyMjQ3OCwxNzAwMjYwMzMzLC03MjA5NjczOTgsLT
U4ODA4NjAsLTIwODg3NDY2MTJdfQ==
-->