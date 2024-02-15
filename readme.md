Inline display:

In this activity we are going to learn how to use the `inline` display. Read carefully the explanation of its characteristics:

       The inline property is the default behavior of some text elements, e.g. <a>, <i>, <b>, <em> and <span>. The elements with this type of display will:
        - Start on the same line of other inline elements next to them.
        - Not be able to change their with or height from the default one, which will be as hight as the content.
        - Not give a layout to its children elements, only to itself.

Now that we know how the `inline` display works, let's start styling the navigation bar on the page indes.html, with the help of our styles.css.

- Step 1:

  - In index.html, inside the `<header>` there are two `<nav>` elements. By default, `<nav>` elements have the `block` display, but we want both our `<nav>` to display on the same line:

    - Go to styles.css and give the `<nav>` ruleset the `display: inline;`.

  - In index.html, inside the `<nav>` elements there are one `<span>` and three `<a>` elements. They are text elements, and have by default the `inline` display. Leave it so.

- Step 2:

  - The`<span>` is supposed to be a logo, so let's make it bigger. In the ruleset for the element inside the styles.css:

    - Give it a width and a height. What is the result?

      `Inline elements aren't affected by height and with, but text elements can alter the size of their content, which gives them its default height.`

    - Give it a `font-size` of 30px.

- Step 3:

  - Making the `<span>` bigger, caused issues with the aligment of the two `<nav>` elements. In the `<nav>` ruleset:

    - Add the `vertical-align`.
    - Test the different values of the property to see what fits: top, bottom, middle, basline.

      `"Inline" and "inline-block" elements can use the "vertical-align property" to align to the content within the default height of the line.`

  - Add the next line of code to the `<nav>`, `<a>` and `<span>` rulesets: `border: 1px solid black;`.
    - Are all the elements correctly aligned?
    - Change the vertical alignment of all the `<a>` and `<span>` elements. What about now?

- Step 4:

  - Let's also give the `<nav>` some whitespace so it doesn't look so cluttered.

    - Add `50px` of `padding`/`margin` to the `<nav>` and the `<a>` elements. What's the result?
    - Add `20px` of `padding`/`margin` to the `<span>`. What's the result?

      `Inline elements will only be affected by margins and paddings horizontally. The vertical padding is going to be there, as you can see thanks to the elements borders, but it will not affect the elements around it`.

  - As vertical `padding` and `margin` will not affect inline element, we can instead target the `<header>`.

    - Refractor the rule for the `<nav>`, `<span>` and `<a>` paddings/margins, so we aren't applying any vertical margin that will not affect our desing anyway.
    - Add `5px` of vertical `padding` to the `<header>` ruleset.

      `<header> elements have the "block" display as default. That means you can alter this element's paddings and/or margins to add that vertical space for the <nav>, <span> and <a> elements not to look so stuck to the top.`

  - Let's do the final touches to our navigation bar by laying out both `<nav>` elements on oposite sites of the viewport

    - Add `750px` of `padding` to the empty ruleset of class selector nav-left.

  - Delete the `border` property that we added before from the `<nav>`, `<span>` and `<a>` rulesets.
