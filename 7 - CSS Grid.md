# 7 - CSS Grid
- Flexbox: simple **1-dimensional** layouts
- CSS Grid: complex **2-dimensional** layouts
  - Columns & rows
  - Global layouts, dashboards...
  - Krachtig en uitgebreid

+ Browser support: sinds maart 2017

## CSS Grid Layout
- Grid container: parent
  - Bepaalt de layout
- Grid items: children
  - Volgen de layout
  - Default source order van de children, maar laat toe om de order zowel verticaal als horizontaal te veranderen

## Grid container
Container is de grid container.
```html
<div class="container">
	<div class="item item-1"></div>
	<div class="item item-2"></div>
	<div class="item item-3"></div>
</div>
```

## Grid item
Item elementen zijn grid items. Sub-item niet.
```html
<div class="container">
	<div class="item"></div>
	<div class="item">
		<p class="sub-item"></p>
	</div>
	<div class="item"></div>
</div>
```

## Grid Line
- Scheidingslijnen die de structuur van het grid bepalen
- Vertical: column grid line
- Horizontal: row grid line

![](https://i.imgur.com/CQWM5x9.png)

## Grid Track
- Ruimte tussen twee opeenvolgende grid lines
- Vertical: columns
- Horizontal: rows

![](https://i.imgur.com/fuyWucn.png)

## Grid Cell
- Ruimte tussen twee opeenvolgende row & column grid lines

![](https://i.imgur.com/DbkzMB7.png)

## Grid Area
- Ruimte tussen twee row & column grid lines
- Kan meerdere grid cells bevatten

![](https://i.imgur.com/WvEMAcH.png)

## Properties voor de parent (container)
- **display:** grid | inline-grid
- **Grid tracks, lines en area's definiëren**
  - grid-template-columns
  - grid-template-rows
  - grid-template-areas
  - grid-template (shorthand)
- **Gap (gutter)**
  - grid-column-gap
  - grid-row-gap
  - grid-gap (shorthand)
- **Alignment**
  - justify-items
  - align-items
  - place-items
  - justify-content
  - align-content
  - place-content
- **auto-generated grid tracks**
  - grid-auto-columns
  - grid-auto-rows
  - grid-auto-flow
- grid (shorthand)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3MDAzODg2MjgsLTEwMzY2MTA3NTRdfQ
==
-->