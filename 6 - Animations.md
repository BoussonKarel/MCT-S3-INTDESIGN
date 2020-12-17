# 6 - Animations
## Transitions
- Geanimeerde verandering tussen 2 status
- User interaction
- Belangrijk onderdeel van User Interface Design
- Micro interactions: hover, clicks, tap, gestures...

+ *bv. Like button wanneer je erop klikt*

## Animations
- Een getimede animatie
- Start zonder dat de user iets doet
- User kan er ook niets aan doen (eventueel pauzeren of stoppen)

+ *Soort filmpje die afspeelt*
+ *Loader*

## Speed
Twee variabelen beïnvloeden dit: **duration** en **easing**
### Duration
- Hoe lang duurt de perfecte transition
- Niet te lang, niet te kort
- Tussen 200ms en 500ms voor interface elementen
- Onder 100ms: nauwelijks zichtbaar
- Boven 1s: te traag, hinderlijk
- Afhankelijk van:
  - grootte object
  - complexiteit
  - afstand (af te leggen)
  - schermgrootte (hoe kleiner je scherm, hoe kleiner de afstand, hoe sneller)


- Material design: alle durations vastgelegd (https://material.io/design/motion/speed.html#duration)

![enter image description here](https://miro.medium.com/max/1000/1*0bES0_PCswamMscW-uUuYg.gif)

![enter image description here](https://miro.medium.com/max/1000/1*HEdB3qH7_M3gCy6Rlh406A.gif)

### Easing
- Progressie van de beweging over tijd (duration)
- Specificeert de versnelling of vertraging
- Duration blijft hetzelfde
- In plaats van een constant (lineair) tempo
- Maakt de animatie natuurlijker
- Geeft de animatie karakter
- Alsof elementen beïnvloed worden door natuurlijke krachten zoals wrijving en zwaartekracht
- 1 van de essentiële **principes van animatie**

+ Natuurlijke vorm van beweging

![](https://miro.medium.com/max/1000/1*JsluHqaqpzaUwSrDaw9-fg.gif)

![Image from Gyazo](https://i.gyazo.com/4a762f14a88405da9c426d4eb82028d7.gif)

### Cubic-bezier curves
- Visualiseren de progressie van de beweging over tijd (duration)
- Timing functions
- 4 punten:
  - p0 en p3: begin en einde
  - p1 en p2: control points
- cubic-bezier(x-p1, y-p1, x-p2, y-p2)

![](https://i.imgur.com/W9gx0XI.png)


### Ease-out
- Decelerate easing
- Begint snel
- Vertraagt naar het einde
- Ideaal voor **inkomende elementen**

![](https://miro.medium.com/max/1000/1*JhyE_rYlaad9DQt6VHFeEA.gif)

### Ease-out extra functions
![enter image description here](https://i.imgur.com/9Hbld5j.png)

### Ease-in
- Accelerate easing
- Begint traag
- Versnelt naar het einde
- Ideaal voor **uitgaande elementen**

### Ease-in extra functions
![](https://i.imgur.com/m4Ly2mX.png)
---
+ OPGELET:
  + EASE-**OUT** VOOR **INKOMENDE** ELEMENTEN
  + EASE-**IN** VOOR **UITGAANDE** ELEMENTEN

### Ease
- Meestvoorkomende soort easing
- Zowel op begin als einde
- Legt nadruk op het einde van de animatie
- Geeft meer tijd aan de vertraging dan aan de versnelling

![](https://i.imgur.com/9Zh54lR.png)

### Ease-in-out
- Begin en einde versnellen en vertragen even snel
- Tenis effect
- Heeft een specifiek karakter
- Ook niet voor elke situatie

![](https://i.imgur.com/yteyRFq.png)

### Ease-in/out-back
- Bounce effect
- Maakt het nog levendiger (anticipation)
- Niet voor elke situatie
- Enkel voor beweging (niet voor color changes)
- Negatieve y-waarde

![](https://i.imgur.com/jw8d9su.png)

## CSS transition
- Automatische animatie tussen 2 verschillende property values
- Keer automatisch terug als de animatie nog niet helemaal gedaan is
- **Altijd op de initiële state declareren**

### CSS transition properties
- **transition-duration:** duur van de animatie in ms of s (required)
- **transition-timing-function:** easing (optioneel)
- **transition-delay:** vertraging vooraleer de animatie start (optioneel)
- **transition-property:** welke property moet er geanimeerd worden (default: all; optioneel)
- **transition:** [transition-property] [transition-duration] [transition-timing-function] [transition-delay];
 
#### transition-timing-function
+ Easing
+ Standard easing names (zijn ook cubic-bezier functies)
  + ease (default)
  + linear
  + ease-in
  + ease-out
  + ease-in-out
+ custom: cubic-bezier(x-p1, y-p1, x-p2, y-p2) (https://matthewlein.com/tools/ceaser)

#### transition-timing-function step values
- step-start instantly jumps to the final state
- step-end stays at the initial state until the end, when it instantly jumps to the final state
- steps(4, end) defines the number of steps before reaching the end. Does not vary gradually, but jumps from state to state.

#### Multiple transitions
 ```css
transition: width 1s ease-in, height 2s ease-out, background-color 3s ease-in-out, transform 4s linear;
```
of
```css
transition-property: width, height, background-color, transform;
transition-duration: 1s, 2s, 3s, 4s;
transition-timing-function: ease-in, ease-out, ease-in-out, linear;
```

## CSS animation


### High Performance Animations
### JS libraries
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzkyODk2NDQxLDQzMDYzMzgyNSwtNTYwNj
QwNzUwLDE2OTE5MzI5ODddfQ==
-->