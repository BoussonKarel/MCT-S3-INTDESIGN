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

<!--stackedit_data:
eyJoaXN0b3J5IjpbOTY2MzgzMzIxLC0xMDM2NjEwNzU0XX0=
-->