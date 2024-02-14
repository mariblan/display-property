Inline display:

In this activity we are going to learn how to use the `inline` display. Read carefully the explanation of its characteristics:

    `inline` - The inline property is the default behavior of some text elements (e.g. <a>, <i>, <b>, <em> and <span>). The elements with this type of display will:
        - Start on the same line of other inline elements next to them.
        - Not be able to change their with or height from the default one, which will be as hight as the content.
        - Not give a layout to its children elements, only to itself.

Now that we know how the `inline` display works, let's start styling the navigation bar on the page indes.html, with the help of our styles.css.

    - Open now the index.html file and look at the code inside the <header> element.
    You can see that there is a <nav> element with an <span> and another one with three <a> tags. <nav> elements have as a default the `block` display, so you will see how in the browser, the content inside each <nav> is in a column disposition.
    Lets change the display for the <nav> in styles.css to `display: inline;`.

    - The elements are in a line now, but the text in the <span> is supposed to be a placeholder for a logo. To make it look like one, add a ruleset for the <span> to make it bigger. What property can you use for that?

            "The `inline` elements cannot be altered by the height and with properites, but text elements can alter the size of their content, which gives them its default height. Add `font-size: 30px;` to make our <span> bigger."

    - Now that the <span> is bigger, the aligment of both <nav> is off. Add `vertical-align: middle;` to the <nav> ruleset to solve it.

            "Inline and inline-block elements can use the `vertical-align` property to align to the content within the default height of the line. This height is stablished by the biggest element in the line. In our case, that is the <span>."

    - Both <span> and <a> elements are aligned correctly now.There is still no whitespace though. The <span> is stuck to the top, right, left and bottom. To see this correctly, give the <nav>, <span> and <a> elements a border(`border: 1px solid black;`).

    - We can see the size of the content now, thanks to our border. We can also observe thanks to it, how the <nav> elements are not actually aligned, only the <span> and <a> tags are. In fact, the <span> is overflowing its parent container. To solve the aligment issue, give `vertical-align: middle` to both the <a> and the <span>.

    - Let's also give the <nav> some whitespace so it doesn't look so cluttered. Add some `padding` or `margin` to give whitespaces to the <nav>, <span> and <a> elements. Test different sizes to see what happens (10px, 20px, 30px, etc.). What was the result?

            "Inline elements will only be affected by margins and paddings horizontally. The padding is going to be there, as you can see for the space left between the border and the elements. However, the vertical paddings will not affect other elements, as if they weren't there. You can notices that in the fact the elements are not been pushed down by the `padding`or `margin` on the top, and the increase in the size is not making the <header> element bigger."

    - As `height`, `width`, `padding` and `margin` will not help us achieve the whitespace by targeting an inline element, we can instead target its parent, the header. Add `padding: 5px;` to its ruleset.

            "The <header> has no display specified in the css, so it is rendering with the default `block` display, as most html do. That means you can alter this element's paddings and/or margins to add that vertical space for the <nav>, <span> and <a> elements not to look so stuck to the top."


    - Now, that the whitespace is added, let's refractor our code to make the final touche's to our navigation bar. Take away the borders to <nav>, <span> and <a> elements.

    - Refractor the padding of the <nav> to `padding: 0 50px;`, so the padding is only applied to the sides.

    - Refractor the padding of the <span> and <a> elements to `padding: 0 20px;`.

    - Add `padding: 290px;` to the empty ruleset of class selector .nav-left. This is going to help the elements to have the most typical layout for navigation bars with two elements.

    - And finalize everzthing by taking away the styling of the <a> tags. Add ` text-decoration: none;` and `color: black;`
