<!-- > :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life. -->

# deep-dive-flex-box

## What is flexbox?

> Flexbox is a CSS box model to easily **layout**, **align** & **distribute space among items** within a **Container** either **horizontally** or **Vertically**.

<!--  -->

> :memo: **Note: Visually explain**.

### Layout

> ![layout](./assets/img/layout.png)

### Align

> ![layout](./assets/img/align.png)

### Distribute space

> ![layout](./assets/img/space.png)

### Container

> ![layout](./assets/img/container.png)

### Horizontally

> ![layout](./assets/img/hrizontally.png)

### Vertically

> ![layout](./assets/img/vertically.png)

## Flexbox have two axis

### **1. Main axis Or x-axis**

### **2. Cross axis Or y-axis**

> ![axis](./assets/img/axis.png)

# Flexbox Properties

> ## **flex-direction**
>
> **The flex-direction property is used to control the direction in which flex items are laid out within a flex container. This property is crucial in creating flexible, responsive designs that can adapt to different screen sizes, orientations, and content needs.**

<!--  -->

> ### **Possible Values of flex-direction:**
>
> ### **flex-direction: row (default)**
>
> **Items are laid out horizontally from left to right.** > ![row](./assets/img/row.png)

<!--  -->

> ### **flex-direction: row-reverse**
>
> **Items are laid out horizontally from right to left (reverse order of row).**
>
> ![row-reverse](./assets/img/row-reverse.png)

<!--  -->

> **Items are laid out vertically from top to bottom.**
>
> ![column](./assets/img/column-4.png)
>
> ### **How to work flex-direction: column?**
>
> **Visually explain:** > ![column](./assets/img/column-1.png)
>
> ![column](./assets/img/column-2.png)
>
> ![column](./assets/img/column-3.png)
>
> ![column](./assets/img/column-4.png)

<!--  -->

> ### **flex-direction: column-reverse**
>
> **Items are laid out vertically from bottom to top (reverse order of column).**
>
> ![column-reverse](./assets/img/column-reverse.png)

<!--  -->

> ## **flex-wrap**
>
> **The flex-wrap property is used in Flexbox layouts to control whether flex items should wrap onto multiple lines or stay on a single line within a flex container. This property is essential for creating responsive layouts where items need to adapt to varying screen sizes or container widths.**

<!--  -->

> ### **Possible Values of flex-wrap:**
>
> ### **flex-wrap: nowrap (default)**
>
> **Flex items will not wrap; they stay on a single line, which may cause overflow if the items exceed the container's width.**
>
> ![nowrap](./assets/img/nowrap.png)

<!--  -->

> ### **flex-wrap: wrap**
>
> **Flex items will wrap onto multiple lines from top to bottom, filling the lines as needed.**
>
> ![nowrap](./assets/img/wrap.png)
>
> ### How to flow wrap?
>
> ![wrap-flow](./assets/img/wrap-flow.png)

<!--  -->

> ### **flex-wrap: wrap-reverse**
>
> **Similar to wrap, but the flex items wrap from bottom to top instead of top to bottom.**
>
> ![wrap-reverse](./assets/img/wrap-reverse.png)
>
> ### How to flow wrap-reverse?
>
> ![wrap-reverse-flow](./assets/img/wrap-reverse%20flow.png)

<!--  -->

> :bulb: **Tip:**
>
> ### When you set flex-direction: column, the flex-wrap property still functions, but its behavior changes because the primary axis is now vertical (from top to bottom), and the cross axis is horizontal (from left to right).
>
> With flex-direction: column, wrapping occurs horizontally across the cross axis, rather than vertically down the primary axis.
>
> Understanding flex-wrap with flex-direction: column:

1. Normal wrapping (flex-wrap: wrap): Flex items will wrap horizontally, creating new columns as needed.

2. Reverse wrapping (flex-wrap: wrap-reverse): Flex items will wrap horizontally in reverse, with new columns forming from right to left instead of left to right.

> ### **flex-direction: column**
>
> ### **flex-wrap: nowrap**
>
> **When you use flex-direction: column combined with flex-wrap: nowrap, the flex items will be laid out in a single vertical column, and they will not wrap to additional columns, regardless of the container's height or the number of items. Instead, the items will overflow the container if they cannot fit within its height.**

### Behavior of flex-wrap: nowrap with flex-direction: column:

1. **Single Column Layout: All items are stacked vertically in one column.**
2. **No Wrapping: Even if there are more items than the container can hold vertically, they will not wrap to additional columns.**
3. **Overflow Handling: If the total height of the items exceeds the container's height, the content will overflow, potentially leading to items being cut off or requiring scrolling.**

> ![column-nowrap](./assets/img/column-nowrap.png)
> :warning: **Warning:**
>
> Managing Overflow: If you use flex-wrap: nowrap with flex-direction: column, it’s important to manage overflow carefully, especially if the container has a fixed height. Adding overflow-y: auto; or similar properties can help ensure that content is accessible even if it extends beyond the visible area.

<!--  -->

> ### **flex-direction: column**
>
> ### **flex-wrap: wrap**
>
> **When you use flex-direction: column combined with flex-wrap: wrap, the flex items are laid out in a single vertical column until they exceed the container's height. Once there isn't enough vertical space to fit additional items, they wrap horizontally into new columns within the container. This means that instead of the items continuing vertically down the page, they will move to the right and start a new column.**

### Behavior of flex-wrap: wrap with flex-direction: column:

1. **Primary Axis (Vertical): Items stack vertically until the container’s height is filled.**
2. **Cross Axis (Horizontal): When the vertical space is exhausted, additional items wrap to a new column to the right.**
3. **Multiple Columns: The layout results in multiple vertical columns of items within the container.**

> ![column-wrap](./assets/img/column-wrap.png)
> :warning: **Warning:**
>
> 1. Container Width: Make sure your container has enough width to accommodate multiple columns; otherwise, the items might overflow horizontally.
>
> 2. Gap Management: Use the gap property to control the spacing between the columns and rows, ensuring the layout remains visually appealing and readable.
>
> 3. Fixed Item Height: If the height of the items is fixed, wrapping behavior will be more predictable. If the height is dynamic, be mindful that wrapping might occur at different points depending on the content.

<!--  -->

> ### **flex-direction: column**
>
> ### **flex-wrap: wrap-reverse**
>
> **When you use flex-direction: column combined with flex-wrap: wrap-reverse, the flex items are still laid out in a single vertical column until they exceed the container's height. However, when wrapping occurs, the additional items are placed in new columns that are added to the left of the original column instead of the right. This creates a reverse wrapping effect.**

### Behavior of flex-wrap: wrap-reverse with flex-direction: column:

1. **Primary Axis (Vertical): Items stack vertically until the container’s height is filled.**
2. **Cross Axis (Horizontal): When the vertical space is exhausted, additional items wrap into new columns on the left side of the existing column, moving in the opposite direction of the normal wrapping behavior.**
3. **Multiple Columns: The layout results in multiple vertical columns within the container, but new columns are created to the left.**

> ![column-wrap-reverse](./assets/img/column-wrap-reverse.png)
> :warning: **Warning:**
>
> 1. Content Flow: The reverse flow might be confusing in traditional left-to-right designs, so use it in contexts where this behavior enhances the user experience.
>
> 2. Container Width: Ensure that your container is wide enough to handle the additional columns on the left side, otherwise the content might overflow horizontally.
>
> 3. Responsiveness: Consider how this layout behaves on different screen sizes, particularly on narrow screens where wrapping might result in very narrow columns.

<!--  -->

> ## **flex-flow**
>
> **The flex-flow property is a shorthand in CSS that allows you to set both the flex-direction and flex-wrap properties in one declaration. This property is useful for simplifying your code and ensuring that both direction and wrapping behavior are defined together.**

### Syntax:

```
flex-flow: <flex-direction> <flex-wrap>;
flex-flow: row wrap; /* Shorthand for flex-direction: row; and flex-wrap: wrap; */
```

> ## **justify-content**
>
> **justify-content is a CSS property that aligns the flex items along the main axis of a flex container. The main axis is defined by the flex-direction property and can either be horizontal (row) or vertical (column). The justify-content property is applied to the flex container, and it helps control the spacing and alignment of flex items within that container.**

<!--  -->

> ### Why Use justify-content?
>
> You would use justify-content to align and distribute space between items within a flex container. This property is particularly useful when you want to:
>
> 1. Center content horizontally or vertically.
> 2. Space items evenly within the container.
> 3. Control the alignment of items when the container's size is larger than the combined size of the items.

<!--  -->

> ### **Possible Values of justify-content:**
>
> ### **justify-content: flex-start (default)**
>
> **Aligns items to the start of the container.**
>
> ![flex-start](./assets/img/flex-start.png)

<!--  -->

> ### **justify-content: flex-end**
>
> **Aligns items to the end of the container.**
>
> ![flex-end](./assets/img/flex-end.png)

<!--  -->

> ### **justify-content: center**
>
> **Centers items within the container.**
>
> ![center](./assets/img/center.png)

<!--  -->

> ### **justify-content: space-between**
>
> **Distributes items evenly, with the first item at the start and the last item at the end.**
>
> ![space-between](./assets/img/space-between.png)

<!--  -->

> ### **justify-content: space-around**
>
> **Distributes items evenly with equal space around them. The space before the first item and after the last item is half the size of the space between items.**
>
> ![space-around](./assets/img/space-around.png)

<!--  -->

> ### **justify-content: space-evenly**
>
> **Distributes items evenly with equal space around them, including before the first item and after the last item.**
>
> ![space-evenly](./assets/img/space-evenly.png)

<!--  -->

> ## **align-items**
>
> **align-items is a CSS property used in a flex container to align flex items along the cross axis (the axis perpendicular to the main axis). The alignment is based on the flex container's height when the flex-direction is set to row (which is the default) or its width when the flex-direction is set to column.**

<!--  -->

> ### Why Use align-items?
>
> You use align-items to control how flex items are positioned along the cross axis of the flex container. This is particularly useful when you want to align items vertically (if the main axis is horizontal) or horizontally (if the main axis is vertical), ensuring that they are consistent regardless of their content size.

<!--  -->

> ### **Possible Values of align-items:**
>
> ### **align-items: stretch (default)**
>
> **Stretches the items to fill the container (default value). If the item's size is auto, it will stretch to fit the container.**
>
> ![align-stretch](./assets/img/align-stretch-1.png)
>
> ![align-stretch](./assets/img/align-stretch-2.png)

<!--  -->

> ### **align-items: flex-start**
>
> **Aligns items to the start of the cross axis.**
>
> ![align-end](./assets/img/align-flex-start.png)

<!--  -->

> ### **align-items: flex-end**
>
> ** Aligns items to the end of the cross axis.**
>
> ![align-flex-end](./assets/img/align-flex-end.png)

<!--  -->

> ### **align-items: center**
>
> **Centers items along the cross axis.**
>
> ![align-center](./assets/img/align-center.png)

<!--  -->

> ### **flex-direction: column**
>
> ### **flex-wrap: wrap**
>
> **When using flex-direction: column and flex-wrap: wrap, the flex container is set up to stack items vertically and wrap them into new columns as needed. In this scenario, the align-items property still controls the alignment of items, but its effect is applied along the horizontal cross axis (the width of the container) rather than the vertical axis.**

<!--  -->

> ### **align-item: stretch**
>
> ![column-align-stretch](./assets/img/column-align-stretch.png)

<!--  -->

> ### **align-item: flex-start**
>
> ![column-align-flex-start](./assets/img/column-align-flex-start.png)

<!--  -->
<!--  -->

> ### **align-item: flex-end**
>
> ![column-align-flex-end](./assets/img/column-align-flex-end.png)

<!--  -->
<!--  -->

> ### **align-item: center**
>
> ![column-align-center](./assets/img/column-align-center.png)

<!--  -->

> ## **align-content**
>
> **align-content is a CSS property used in flexbox layouts to align flex lines (rows or columns) within the flex container when there is extra space in the cross axis. Unlike align-items, which aligns individual flex items within their flex line, align-content aligns the entire set of flex lines relative to the flex container's cross axis.**
>
> ### Why Use align-content?
>
> You use align-content to manage how multiple flex lines are distributed and aligned within the flex container. This property becomes relevant when you have more than one line of flex items (i.e., when flex-wrap: wrap is used), and it allows you to control the spacing and alignment of these lines.

<!--  -->

> ### **Possible Values of align-content:**
>
> ### **align-content: flex-start**
>
> **Aligns flex lines to the start of the cross axis (top if the main axis is horizontal).**
>
> ![align-content-flex-start](./assets/img/flex-start.png)

<!--  -->

> ### **align-content: center**
>
> **Centers flex lines along the cross axis.**
>
> ![align-content-center](./assets/img/align-content-center.png)

<!--  -->

> ### **align-content: space-between**
>
> **Distributes flex lines evenly with the first line at the start and the last line at the end of the container.**
>
> ![align-content-space-between](./assets/img/align-content-space-between.png)

<!--  -->

> ### **align-content: space-around**
>
> **Distributes flex lines evenly with equal space around them. The space before the first line and after the last line is half the space between lines.**
>
> ![align-content-space-around](./assets/img/align-content-space-around.png)

<!--  -->
<!--  -->

> ### **align-content: space-evenly**
>
> **Distributes flex lines evenly with equal space between all lines, including before the first line and after the last line.**
>
> ![align-content-space-evenly](./assets/img/align-content-space-evenly.png)

<!--  -->
