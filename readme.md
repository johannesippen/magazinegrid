# Using magazine grid

magazine grid will help you create nice magazine layouts in HTML5 for the iPad. It creates an 8-column grid and some typographic styles.

## Grid numbers

The grid consists of 8 columns with a width of 82 pixels in portrait & 114 pixels in landscape orientation. They have a gap of 16 pixels. It comes with a fix baseline grid of 22 pixels and an optional gutter of 49 pixels.

## Setting up

To use magazine grid, you need to include only CSS File. It's highly recommended to use the minified Version. Also, you need to set the viewport width to prevent automatic scaling of your page. Include the following code into the <head> of your page:

	<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0;">
	<link rel="stylesheet" href="magazinegrid.min.css" type="text/css" media="screen, handheld" charset="utf-8">

## HTML

	<article>
Will be the wrapper for the page. Be aware that all other features of magazine grid will only work inside an article-element

	<nav class="pagina">
Put this as the first element inside the ´<article>´. Will format as a Pagination, possibly to put the category or page number.

	<section>
Defines a new "row" of elements. 

	<p class="grid x1">
Defines an element inside the grid which is one column wide. Feel free to use every semantic element you like.
Following classes are possible:
	
- ´grid´ - makes the element a part of the grid
- ´x1-8´ - defines the width of the element. Can be between one and eight columns wide
- ´indent1-7´ - pushes an element one column to the right. Can be between one and seven.

### Typography

	<section class="gutter">
Defines an element with a nice gutter to enhance rich text formatting. Following classes are possible:

- ´gutter´ - sets a gutter of 0.5 columns on both sides of page
- ´column2´ - formats the text in 2 columns
- ´column3´ - formats the text in 3 columns
- ´column2 border´ - formats the text in 2 columns, justified & with a thin border between the gaps
- ´column3 border´ - formats the text in 3 columns, justified & with a thin border between the gaps
	
### Example HTML

	<article>
		<nav class="pagina</strong>">…</nav>
			<section>
				<p class="grid x4">
					Paragraph Element, 4 columns wide
				</p>
				<p class="grid x2 indent1">
					Paragraph Element, 2 columns wide, pushed 1 column to the right
				</p>
				<h1 class="grid x1">
					Headline Element, 1 column wide
				</h1>
			</section>
			<section class="gutter column2">
				<p>
					Text running in 2 columns with gutter left/right of 0.5 grid columns
				</p>
			</section>
	</article>
