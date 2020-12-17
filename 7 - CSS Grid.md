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

## Properties voor de child (items)
- **Locatie binnen de container**
  - grid-column-start
  - grid-column-end
  - grid-row-start
  - grid-row-end
  - grid-column
  - grid-row
  - grid-area
- **Alignment**
  - justify-self
  - align-self
  - place-self

## grid-gap
- Gutter tussen opeenvolgende items (niet links of rechts, boven of onder)
- grid-column-gap
- grid-row-gap
- grid-gap: [row-gap] [column-gap]

## grid-template-columns / grid-template-rows
- Definiëren de columns en rows
- Meerdere values gescheiden door spaties
- De values staan voor de track size
- De spaties staan voor de grid lines
- **track-size:** auto, px, vh, vw, % of een fraction van de overgebleven ruimte: **fr**
- **line-name:** automatische positieve en negatieve nummers. Maar je kan die zelf een naam geven om bij een item op te roepen.

## Automatische line-names
```css
grid-template-columns: 40px 50px auto 50px 40px;
grid-template-rows: 25% 100px  auto;
```
![](https://i.imgur.com/EytuTh8.png)

```css
grid-template-columns: [first] 40px [line2] 50px [line3] auto [col4-start] 50px [five] 40px [end];
grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];
```
![](https://i.imgur.com/AiGGf7c.png)

## grid-template-columns / grid-template-rows
- **Track size special notations**
  - 1fr: fraction unit: 1 deel van de  overgebleven ruimte
  - auto: neemt de breedste of hoogste content als basis voor de breedte of hoogte
  - repeat(12, 1fr): maakt 12 kolommen aan van 1fr
  - minmax(260px, 1fr): maakt 1 column of row aan van minimum 260px en maximum 1fr
  - auto-fit en auto-fill keywords: responsive grid system without media queries
  - **Combinaties:** grid-template-columns: minmax(150px, 1fr) auto 1fr;
    - 1 column van min.150px en max. 1fr
    - 1 column die automatisch de breedte van de content krijgt
    - 1 column van 1fr

## grid-column-start, grid-column-end, grid-row-start, grid-column-end, grid-column, grid-row
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU2NDc3MDcxMCwtMTAzNjYxMDc1NF19
-->