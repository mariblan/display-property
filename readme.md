Step 1 - display:
The display property of css specifies how the element itself, or its children elements, are going to layout on the page.
There are 8 types of displays, and each ones has a different behavior, so lets use the navigation bar on index.html to tests them.

First, we are going to work with the `block`, `inline-block` and `inline` values. Read carefully the explanation of each element:

    `block` - The block property is the default behavior for most elements. The elements with this type of display will:
        - Start on a new line from the previous element.
        - Take the whole with of the viewport.
        - Be as hight as its content. If there is no content inside, they will have no hight and will not display.
        - Be able to add paddings and margins vertically.

    `inline` - The inline property is the default behavior of some text elements (e.g. <a>, <i>, <b>, <em> and <span>). The elements with this type of display will:
        - Start on the same line of other inline elements next to them.
        - Not be able to change their with or height from the default one, which will be as hight as the content.

    `inline-block` - The inline-block property combines the behavior of the both displays. The elements with this type of display will:
        - Stack horizontally as the inline elements.
        - Be able to change their with and height as the block.

Something that is also important, is that the display is applied to the element that we want to make display inline with others or on the next line.

With that said, lets start by applying the `inline` display to our navigatio bar:

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



Dipslay `Block`


    - which makes the text stuck to the top and left side. Add `vertical-alignment: middle;`, `height: 80px;` and `padding: 10px;` to the ruleset of the <nav> elements.



    - The content of the <hav> has aligned itself to the middle of the container and, but the height remained unchanged and the padding hasn't applid to the top and bottom. That is because inline elements can't change their height or with, and can only manipulate the horizontal whitespace, but not the vertical (padding-top, paddint-bottom, margin-top, margin-bottom).
    For the height and padding property to apply, change the display of the <nav> to `display: inline-block;` instead.

    - Wait, now the <nav> has change its height, but the <img> and the <a> elements are not aligning correctly anymore. Try adding `vertical-alignment: middle;` to both elements' rulesets.

    - Both the <img> and the <a> elements are aligning vertically, but only inside their own line height that is preset by the size of the content inside. This content size can be afected by font-size or, in the special case of images, by the with or height set for the <img>. To understand that, add `border: 1px solid black;` to the <img> and <a> tags and `height: 40px;` to the <img> tag.

    - You can see here that the <a> elements are aligning to the middle of the height preset by the line, that has now increased by making the <img> bigger. However, that hasnt change the alignment within their parent element, the <nav>. Also, we might not want to have to increase the

    - See? Both <img> and <a> elements are align to the middle vertically within their boxes. However, they are not centering themselves withing the <nav>. Let's try to apply some paddings and margins. Did that help?

    -

    - As the <a> are inline elements, they can't change their height, and therefore, they are stack to the top of the <nav> and refusing to align to the middle. The <img> is changing it's sizing, but it is also not aligning to the middle. That

Step 2- background-image:

    1.1. Go to the class hero, and add the propertygit
