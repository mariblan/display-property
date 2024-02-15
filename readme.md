CSS - Display property:

The `display property` specifies the display behaviour of an element, that is, how it is going to be laid out or if it is even going to be visible at all.
There are 8 types of values you can pass to the `display property`:

`none` - The element will not display.

`block` - it is the default display for most html elements. Block elements always will:

- Start on a new line.
- Take the whole with of the viewport.
- Be as hight as its content. If there is no content inside, they will have no hight and will not display.
- Be able to add paddings and margins vertically and horizontally.

`inline` - It is the default behaviour of some html elements (mostly text elements), e.g. span, a and b element. Inline elements will:

- Display on the same line as the previous element, ocupaying only one line.
- Not be affected by the `width` and `height` properties.
- Be able to add `padding` and `margin`, but they will only take effect horizontally.

`inline-block` - It combines the behavior of the both previous displays. Inline-block elements will:

- Stack horizontally as the inline elements.
- Be affected by `with` and `heigh`. - Be able to add `padding` and `margin` both horizontally and vertically.

`flex` - It turns the element into a flex-container, and all its direct children to flex-children. Flex-containers will:

- Behave as block elements, starting always in a new line.
- Use other flex properties to alter the default behavior of the flex-container and its flex-items.
  Flex-childre, also called flex-items, will:
- Position and size themselves according to the container they're in.
- Use other properties to alter the behavior established by the flex-container for them.
- Be able to adapt its layout depending of the screen size.

`inline-flex` - As the `flex` display, it turns the element into a flex-container, and all its direct children to flex-children. The inline-flex-container will:

- Behave as inline elements.
- Use other flex properties to alter the default behavior of the flex-container and its flex-items.
  Flex-childre, also called flex-items, will:
- Position and size themselves according to the container they're in.
- Use other properties to alter the behavior established by the flex-container for them.
- Be able to adapt its layout depending of the screen size.

`grid` - It turns the element into a grid-container, and all its direct children to grid-children. The grid container will:

- Behave as block elements, starting always in a new line, but with a grid layout for its children.
- Use other grid properties to alter the default behavior of the fgrid-container and its grid-children.
  Grid-children, will:
- Position and size themselves according to the grid layout of the grid-container they're in.
- Use other properties to alter the behavior established by the grid-container for them.

`inline-grid` - It turns the element into a grid-container, and all its direct children to grid-children. The grid container will:

- Behave as inline elements, but with a grid layout for its children.
- Use other grid properties to alter the default behavior of the fgrid-container and its grid-children.
  Grid-children, will:
- Position and size themselves according to the grid layout of the grid-container they're in.
- Use other properties to alter the behavior established by the grid-container for them.

With that said, lets start aplying some of this displays in the next ativities, so we can undestand better how to use them.

Step 2 - Background properties:

The background of an element is the total size of the element, including padding and border (but not the margin). The are many background properties that can help to style it:

`background-color` - sets the background color of an element.

`background-image` - sets one or more background images for an element. For this, it uses the url() css function to add relative paths or urls:

        body {
        background-image: url("img_tree.gif"), url("paper.gif");
        background-color: #cccccc;
        }

By default, a background-image is placed at the top-left corner of an element, and repeated both vertically and horizontally to cover the whole element.

`background-repeat`- sets if/how a background image will be repeated.

`background-size`- specifies the size of the background images.

Step 3 - Position property:

The `position property` defines the positioning method used by an element. With position, to specify the exact position on the screen, we need to use the top, bottom, left and right properties. Not all of them have to be used for the position to work.
There are 5 types of values you can pass to the `position property`:

`static` - It is the default position for elements, following the normal flow of the page. It is not affected by the top, bottom, left and right properties.

`absolute` -It defines the position of the element relative to the nearest positioned ancestor. If there are no positioned ancestors, it will use the body's position instead. It also removes the elements from the normal flow and can make them overlap other elements.

`relative` - It defines the position of the element relative to its normal position (the static). Other content will not be adjusted to fit in the gap left by the element.

`fixed` - It defines the position of the element relative to the viewport, making it always stay in the same place.
Fixed elements don't leave a gap, they can stack on top of or under other elements depending on their z-index.

`sticky` - It defines the position of the element relative to the user’s scroll position, making the element toggle between relative and fixed position: it will be relative until a given offset position is met in the viewport, and then it will be fixed.  
Using top, bottom, left and/right will cause it to be adjusted out of its normal position.
