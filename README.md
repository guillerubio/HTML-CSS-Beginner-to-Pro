# [HTML & CSS Full Course - Begginer to Pro](https://www.youtube.com/watch?v=G3e-cpL7ofc&t=1787s)

## HTML Basics

HTML stands for Hyper Text Markup Language and CSS for cascading style sheets. 

Concepts:
1. Element: HTML building block, it is enclosed in tags
2. Tag: syntactical object we use to enclose elements: `<p></p>`
3. Attributes: properties of elements enclosed in the opening tag `<div class=“hello”>`, they modify the behaviour of elements.
***

## CSS Basics 

CSS stands for Cascading Style Sheets, it is used to change the apperance of HRML elements.

To write CSS we must have a `<style>`element

Concepts:
4. CSS selector: represent which element we are targeting to style. `button { }` This code targets all buttons in the page.
5. CSS property: tells the computer what are we changing: `background-color:`
6. CSS value: tells the computer what we are changing the property to `red`.

All together it looks like this (YT Subscribe button):

``` Css
<style>
  button {
    background-color: rgb(200, 0, 0);
    color: white;
    border: none;
    height: 36px;
    width: 105px;
    border-radius: 3px;
    cursor: pointer;
  }
</style>
```

You do not have to know all the CSS properties, you can just use Google.

7. HTML class attribute:  `<button class="">` let's us label HTML elements, and target them. Very useful in CSS.

To target a class in CSS, the CSS selector must start with a dot: `.subscribe-button {...}`. Multiple elements can have the same class.

8. Space: in CSS space between elements is called margin

```
General Technique: 
1. Create element with HTML.
2. Style with CSS one-by-one.
```
***
## Hovers, Transitions and Shadows 

Most buttons on the internet change their style when you hover your mouse hover them. They do it smoothly (transitions) and some of them also cast shadows.

To apply styles on hover, we create a new CSS class selector with the `.hover` pseudo-class  like this: `.subscribe-button:hover {...}`

9. Pseudo-class: It **adds** extra styles in certain situations. `.subscribe-button:hover {...}` some examples are: `hover`, `active` etc.

10. Transition properties: Takes two arguments, the CSS property that will change with pseudo-classes, and the amount of time it should take to change them: 
``` Css
transition: background-color 1s,
      color 1s;
```

11. Box-shadow: CSS property to cast element shadows, it takes four arguments: horizontal vertical blur color: `box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);`

12. RGBA: Same as RGB bit with opacity value 1 to 0.

***
## Chrome DevTools & CSS Box Model

13. Chrome DevTools: Useful tool in browsers too visualize the HTML and CSS attributes. We can use it to copy exact colors, styles etc.
Note: Chrome developer tools gives colors in hex value, it is just the three RGB values but in hexadecimal

14. CSS Box Model: Tool that alows us to add space between elements. And condition the space inside the element itself. It's importance derives on the fact that the contents inside of elements is bound to change, this way the size of elements is adjusted based on it's content, with no need for manual resizing

CSS box model composed of: 

15. Margin: Spacing on the outside of the element. We can add margin to the four sides of the elements. `margin-left`, `margin-right`, `margin-top`, `margin-bottom`. 
16. Padding: spacing on the inside of an element. We can add margin to the four sides of the elements. `padding-left`, `padding-right`, `padding-top`, `padding-bottom`. 
17. Border: visible or invisible line between margin and padding. We can control it with CSS attributes such as: `border-color`, `border-style`, `border-width` etc.

18. Vertical-align: By default, browsers will align elements on text basis. To overide this behavior we can use the `vertical-align: top;` attribute. 

NOTE: border adds to the element size, adjust padding acordingly.
 
***
## Text Styles

We can control text styles using CSS properties like this:
```CSS
.video-title {
  font-family: Arial;
  font-size: 18px;
  font-weight: bold;
  font-style: italic;
  text-align: center;
  width: 300px;
  line-height: 24px;
}
```
To know all of thes properties, you can use Google.

19. HTML entity: special HTML characters like stars &#9733;, middle dots &#183;, checkmarks &#10003; etc. (Find in Google)

Notes: 

- `<p>` by default, come with margin at the top and bottom. 
- To re-space text components we reset the spacing between them to 0 and use the `margin-bottom` of the one on top.
- We can style all paragraphs in a page by using the css selector `p {...}`. This means that an element can be targeted by multiple sets of styles. This is also very useful to reset all margins
- With multiple sets of styles applied, if we change the same property, wich one is applied? The mone with the most specific selector.
- Greater than and less than should be added to html content with HTML entities to prvent browsers from messing up compiling.

20. Text elements: element inside a line of text that modify a part of the text. There are multiple text elements:

1. `<strong></strong>` Makes some text bold.
2. `<u></u>` Makes some text underlined.
3. `<span></span>` Generic text element able to have a class so that we can target it using CSS. 

***
## The HTML Structure

The HTML structure is composed of
1. `<!DOCTYPE html>`: Tells the browser to use our current HTML version
2. `<html></html>`: Delimits the HTML file
3. `<head></head>`: Nested inside html tags. Contains the elements that aren't on the page. You use elements such as `<title></title>` or `<style></style>`. However, it is a better practice to use a link element instead of the style one.
4. `<body></body>`: Nested inside html tags. Contains all visible elements on the page

HTML structure example:
```Html
<!DOCTYPE html>
<html>
  <head>
    <title>Buttons exercise</title>
    <link rel="stylesheet" href="styles/buttons.css">
  </head>
  <body>
    <button class="subscribe-button">
    SUBSCRIBE
    </button>
  
    <button class="join-button">
      JOIN
    </button>
  
    <button class="tweet-button">
      Tweet
    </button>
  </body>
</html>
```

Notes: 
- The HTML structure is needed to use Live Server.
- You can import custom fonts using link. [Google Fonts](https://fonts.google.com) can give you the code directly.

Concepts:
 
21. Link element: `<link>` Void element (does not require closing tag), with two attributes: `rel` what are we linking (relationship) and `href` the actual link.

***
## Images and Text Boxes
 
Concepts:

22. Image element `<img>` void element that takes one attribute `src` and displays an image

23. `object-fit` property: It is a img specific attribute used to determine what happens when the img dimensions do not match the image's shape. Some of the possible values to this property are `cover`, which tells the img to cover the HTML area keeping it's shape or `contain`, which tells the img to display fully contained in the size specified

24. `object-position` property: Another img specific property used to determine which part of the img we want to view in the case our img object does not fit in the determined area

25. Text box: used to recieve text input on a webpage. It is represented by the `<input>` void element. It recieves a `type` attribute whose value can be `="text"`,
`="checkbox"`, etc.

26. Place-holder: text inside of textboxes that dissapear when user inputs text indicating what that field is for. It is set with the `placeholder=""` attribute.

Notes:

- When we set width or height exclusively, `<img>` keeps aspect ratio, however, if we set width and height, it looses it. 

***
## CSS Display property

In CSS there are three types of elements:

27. Block elements: take up the entire line **in their container**, some examples (by default) include: `<p></p>`.

28. Inline-Block element: only takes up as needed, some examples (by default) include `<img>` or `<input>`.

29. Inline-Element: appear within a line of text, some examples include: `<strong></strong> or <span></span>`.

These elements determine how elements are displayed in the screen

30. `display` property: CSS property that let's us change elements to `block` and `inline-block`.

Note: To target two equal elements on CSS, we can use this sintax: 
```Html
.video-author, 
.video-stats {
  display: inline-block;
}
```
***
## The `<div>` element: *The most important HTML Element*

31. `<div></div>` element: HTML element that stands for division, it is basically a box that surrounds content. By default, it is a block element. It can contain any other elements inside. They are ment to be containers that group related elements.

Notes:
- When block elements are placed inside a `div`, it takes up the entire line inside its container.

***
## Nested Layouts Tecnique: *The most important part of the tutorial*

32. Nested Layouts Tecnique: Based on the broken-down nested combination of vertical and horizontal layouts. In this approach, column and horizontal blocks are represented by div divs. With their `display`property adjusted acordingly.

33. Font-Stack: When selecting the `font-family` value, you can use this sintax to get backup fonts: `font-family: Roboto, Arial;

***
## CSS Grid

34. CSS Grid: A much better way to create horizontal layouts, as well as to create different grids, like youtube video previews one. It is a layout that has rows and columns. To create grids, we use this sintax:
```html
<div style="
      margin-top: 30px;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      column-gap: 20px;
      row-gap: 40px;
      ">
      <div style="background-color: lightblue; height: 200px;">div 1</div>
      <div style="background-color: lightpink; height: 200px;">div 2</div>
      <div style="background-color: lightblue; height: 200px;">div 3</div>
      <div style="background-color: lightpink; height: 200px;">div 4</div>
      <div style="background-color: lightblue; height: 200px;">div 5</div>
      <div style="background-color: lightpink; height: 200px;">div 6</div>
    </div>
```
The number of columns is defined by the number of arguments `grid-template-columns` has. If we put more divs than columns are defined, they start to wrap around.

Notes:

- There are some alignment issues with inline-blocks, mainly, that there is space between the horizontally disposed elements (divs), caused by the new line character in the code which makes it readable.

- You can style components directly in the body of the HTML by using the `style` attribute. This is called inline styling.

- In grids, if you want to use up the remaining amount of space, you can use the special space value 1fr, instad of 30px. If you place multiple columns with 1fr, they will divide the space evenly. It works as a ratio.

- For spacing between columns and rows, we use the `column-gap` and `row-gap`attributes.

***
## Flexbox

35. Flexbox: a similar component to CSS Grid, but it's more flexible. 

36. `justify-content` property: flexbox property that can align the flexbox elements horizontally: to the left `start`, right `end`, center `center` or evenly distributed `space-between`.

37. `align-items` property: flexbox property that can align the flexbox elements vertically up `start`, down `end` or center `center`.

38. `max-width` property: flexbox property that can limit the width of a flexible section of a flexbox

Ways in which flexboxes defere from grids:
- Their size adapts to their content, while grids don't.
- The layout is more rigid for grid, if we change the order of the elements of fb, the elements change the layout, it creates fLeXiBlE layouts.

Ways in which flexboxes are similar to grid:
- They mantain horizontal alignment.
- They have use flex:1 / 1fr values

Example:

```Html
<div style="
      margin-top: 30px;
      display: flex;
      flex-direction: row;
      height: 70px;
      border-width: 1px;
      border-style: solid;
      border-color: gray;
      ">
      <div style="
        background-color: lightblue;
        width: 100px;
      ">100px</div>
      <div style="
      background-color: lightpink;
      width: 100px;">
        100px</div>
      <div style="
        background-color: lightblue;
        width: 100px;
      ">100px</div>
    </div>
```

Notes:

- `flex: 1` is the flexbox equivalent to `1fr`
- A very adequate time to use flexbox is in the Youtube header, when your picture can change sizes because you sign out and now the wign in button is present. Flexbox are used when layouts are bound to change.

***
## Nested Flexbox

39. Nested Flexbox: one flexbox inside of another. By default, `<div></div>` inside flexboxes are not also flexboxes, to use `flex:1` on the components inside the div, you must convert their parent to flexbox using `display: flex`. It is useful to nest flexboxes if you need the middle of the middle either horizontally or vertically.

40. `flex-shrink: 0;` property: Flexbox property that limits the amunt the flexbox is allowed to shrink.

***
## CSS Position

41. `position` property: CSS property that helps us keep the header at the top of the page while we scroll, keep the sidebar at the side of the page, or force an element on top of another element like the notificatioon number on top of notifications icon. Some of the values of this property include `static`: moves with the page, active by default; `fixed`: fixed to it's position on the page, scrolling does not affect it, also it does not take space in the page anymore, it is floating above the page. The position property has other related properties:
- `top`: specifies how far away our element is from the top of the window.
- `left`: specifies how far away our element is from the left of the window.
- `right`: specifies how far away our element is from the right of the window.
- `bottom`: specifies how far away our element is from the bottom of the window.

If we set these properties together, the element streches. 

Note: To add a border to one side only we can use the `border-bottom` etc. property, whos sintax is the same as the `border`

Example 

```Html
<div style="
      background-color: black;
      color: white;
      position: fixed;
      top: 0;
      left: 0;
      right:0;
      height: 50px;
      ">
      header
</div>
```
***

## Position Absolute and Relative

42. `position: absolute` property value: CSS value that takes the same related properties as `position`: `top`, `left`, `right`, `bottom`. However, this property value presents a key difference with `position: fixed`. `position: fixed` is placed on the browser window (does not move with scroll) while `position: absolute` is placed on the page (moves with scroll). It is used to place an element in a precise position on the page.

Example: 
```Html
<div style="
      position: absolute;
      background-color: red;
      color: white;
      right: 0;
      top:0;">
      X
</div>
```

43, `position: relative` property value: If we want to have a `position-absolute` element  placed relative to it's parent element, it's parent element needs to have the `position: relative` property value.

Note: generally an element that is written below is going to appear in front of elements written in front of it. We can override this behavior with the `z-index: 1`. More z-index means it is higher on th z axis of the page.

## Project finish

Notes:

- In CSS we can combine selectors together with a `,` to target both or with a `space`to target the class inside a class.
- REMINDER: to center things inside an element you use `justify-content` and `align-items`, but it must be a flexbox.
- If ypu have a tooltip coming out of a button, and do not want the tooltip to activate itself when hovering over the tooltip area (not the button, but the tooltip), you can disable this by using the `pointer-events: none;` value on the parent element.

Tooltip example:

```Css
.search-button .tooltip {
  background-color: gray;
  position: absolute;
  color:white;
  padding: 4px;
  padding-left: 8px;
  padding-right: 8px;
  border-radius: 2px;
  font-size: 12px;
  bottom: -30px;
  left: 1px;
  opacity: 0;
  transition: opacity 0.15s;
  pointer-events: none;
}

.search-button:hover .tooltip {
  opacity: 1;
}
```

- We use `white-space: nowrap;` to prevent text from wrapping around












