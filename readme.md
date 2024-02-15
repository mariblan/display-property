Display `inline-block`:

In this activity we are going to learn how to use the `inline-block` display. Read carefully the explanation of its caracteristics:

    `inline-block` - The inline-block displacombines the behavior of the both displays. The elements with this type of display will:
        - Stack horizontally as the inline elements.
        - Be able to change their with and height as the block.
        - Not give a layout to its children elements, only to itself.

Now that we know how the `inline-block` display works, let's start styling the footer on the page index.html, with the help of our styles.css.

- Step 1

  - In index.html, the `<footer>` element has two `<div>` elements, which are been displayed as block elements, as it is their default. We want them to render next to each other though. In styles.css, in the footer section:

    - Add to the `<div>` elements inside the footer a `inline` display. What is the result?

      `Inline display will not work on elements that have block elements as children, as they will not be able to be render in one line. For those, we have the inline-block display, which will let the children elements display as block elements, but the current element will display as an inline one.`

    - Change the `inline` to an `inline-block`.

- Step 2:

  - Let's give a beetter styling to the `<div>` elements so they won't look so cluttered and better aligned. If you need to, add a border to the `<div>` elements to visualize better their size and position.

    - Add `30px` of `padding`.
    - Add `50px` of `margin`.

  - Add now the `vertical-align` property, to aling both elements to the middle.

  - Give both `<div>` elements a `height` of `100px`.
