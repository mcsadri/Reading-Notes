# More CSS Layout (how about no?)

## Learn CSS with Flexbox, it'll be fun they say

What is it? Flexbox is a layout mechanism designed for laying out groups of items in one dimension.

### What can you do with a flex layout?

> - They can display as a row, or a column.
> - They respect the writing mode of the document.
> - They are single line by default, but can be asked to wrap onto multiple lines.
> - Items in the layout can be visually reordered, away from their order in the DOM.
> - Space can be distributed inside the items, so they become bigger and smaller according to the space available in their parent.
> - Space can be distributed around the items and flex lines in a wrapped layout, using the Box Alignment properties.
> - The items themselves can be aligned on the cross axis.
> - ([from web.dev](https://web.dev/learn/css/flexbox/#what-can-you-do-with-a-flex-layout))

### The main axis and the cross axis

> - The main axis is the one set by your flex-direction property.
>   -If that is row your main axis is along the row, if it is column your main axis is along the column.
> - Flex items move as a group on the main axis.
> - The cross axis runs in the other direction to the main axis, so if flex-direction is row the cross axis runs along the column.
> - You can do two things on the cross axis.
>   - You can move the items individually or as a group so they align against each other and the flex container.
>   - If you have wrapped flex lines, you can treat those lines as a group in order to control how space is assigned to those lines
>   - the main axis follows your `flex-direction`
> - ([from web.dev](https://web.dev/learn/css/flexbox/#the-main-axis-and-the-cross-axis))

### Creating a flex container

> - To use flexbox you need to declare that you want to use a flex formatting context and not regular block and inline layout. Do this by changing the value of the `display` property to `flex`.

``` css
.container {
  display: flex;
}
```

> - This will give you a block-level box, with flex item children. The flex items immediately start exhibiting some flexbox behavior, using their initial values.
> - All CSS properties have initial values which control how they behave "out of the box" when you haven't applied any CSS to change that initial behavior. The children of our flex container become flex items as soon as their parent gets `display: flex`:
> - ([from web.dev](https://web.dev/learn/css/flexbox/#creating-a-flex-container))

### Controlling the direction of items

> - Even without the `flex-direction` property he items display as a row because the initial value of `flex-direction` is `row`
> - To change the direction, add the property and one of the four values:
>   - `row`: the items lay out as a row.
>   - `row-reverse`: the items lay out as a row from the end of the flex container.
>   - `column`: the items lay out as a column.
>   - `column-reverse`: the items lay out as a column from the end of the flex container.
> - ([from web.dev](https://web.dev/learn/css/flexbox/#controlling-the-direction-of-items))

#### Reversing the flow of items and accessibility

- doodah

---

1. Flexbox is designed for one-dimensional content. Explain what this means. **Flexbox layouts can display as a row, or a column**
2. Explain the difference between the main axis and cross axis. **The main axis is the one set by your flex-direction property. If that is row your main axis is along the row, if it is column your main axis is along the column.**
3. How can using certain properties of flexbox negatively impact accessibility? **The `row-reverse` and `column-reverse` values are a good example of this. The reordering only happens for the visual order, not the logical order. Screen readers use the logical order to read out content.**

---

this is dreadfully incomplete.
