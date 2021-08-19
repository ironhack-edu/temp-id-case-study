![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# CSS | Advanced Selectors

## Description

In this lesson you will use different CSS selectors to make your simple HTML file from the pre-work a bit more exciting. You will first learn about some of the basic selectors and then progress onto advanced selectors, gaining understanding of when to use them and why. One of the goals of this lesson is to teach you to keep the HTML as tidy, clean, and compact as possible. CSS selectors will help you target elements without having to add classes everywhere, allowing for readable and clear HTML.

## Learning goals

By the end of this lesson, you will be able to:

- Understand why selectors are used in CSS
- Understand when to use different selectors and why
- Select elements using basic selectors
- Select elements combining different selectors
- Select elements based on their relationship to other elements
- Select elements based on their attributes

## Schedule

Today’s lesson will have the following schedule:

* Introduction & Recap - 10'
    * Connect to previous session
    * Recap on document trees
    * Short introduction to CSS Selectors
* Pre-work review - 5'
    * Quick review of pre-work and short show and tell
    * Answer any initial questions
* Guided Examples - 40'
    * Quick review of pre-work and short show and tell
* Break - 10'
* Experimenting with Selectors - 25'
    * Self-led learning
    * Apply different selectors to your pages
* Student Exchange - 10'
    * Short dynamic in pairs to share your work
* Reflection & Discussion - 15'
    * Evaluate key learnings
    * Real-world examples
* Next Steps & Closing - 5'
    * Assessment and evaluation
    * Answer final questions

## Introduction & Recap

### Document Object Model

Before learning about combined CSS selectors, it's a good idea to understand the document tree in the Document Object Model. If you understand the document tree concept, then CSS selectors will be much easier to understand and therefore apply.

All HTML documents can be represented as trees. Each level of the tree is described in the same manner as a human family tree, with ancestors, descendants, parents, children and siblings. CSS selectors can describe elements in the document tree.

For example, in any HTML document, the <body> element is the ==ancestor== of all other elements shown on the page. On the contrary, a ==descendant== refers to any element that is connected but lower down the document tree - no matter how many levels lower.

Parents and children work the same. A ==parent== is an element that is directly above and connected to an element in the document tree; a ==child== is directly below and connected to an element in the document tree.

```html
<ul>
  <li class="menu-item"></li>
  <li class="menu-item"></li>
</ul>
```

In this example, the `<ul>` is a parent to every `<li>` . Those `<li>` elements are its children.

## Why CSS Selectors?

We use [CSS selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors) to find or “select” the HTML elements you would like to style. You will see that they can be used to select fine-grained specific elements, which can be useful when you want to add styling to a particular element according to its id, class, type and attributes.

## Pre-work

Here is an example HTML page in [codepen](https://codepen.io/ollie-j-j/pen/xxdoWpN?editors=1100) which is ready to have some CSS added. If you have yours ready, open your project in your code editor or make a new codepen project.

## Basic Selectors

To begin with, let’s take a look at some basic selectors and how they are used.

### Type Selector

The CSS [type selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors) selects all of the elements of the given type within the document. Choose a type of element in your HTML page to change, I am going to change the `h5` elements in my page to red:

```css
h5 {
  color: red;
}
```

You can see what has happened here in the [codepen](https://codepen.io/ollie-j-j/pen/xxdoWjo) example.

### Universal Selector

The CSS [universal selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors) selects all elements of any type. Targeting all of the elements on the page has a few specific use cases, such as changing the font or  resetting default browser styling. Let’s change the font in our project:

```css
* {
  font-family: sans-serif;
}
```

Let’s also try and visualise all of the different elements on the HTML page. We can do this by adding a border to each element:

```css
* {
  border: 1px solid blue;
}
```

You might not want to include this in your final design, but you can see how all of the elements have been modified in the [codepen](https://codepen.io/ollie-j-j/pen/KKmjoBe) example. Have a go at using the universal selector in your page.

### Class Selector

The CSS [class selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) matches elements based on the contents of their class attribute. In the example there is a class attribute set to `‘heading-background’`. In order to select this element, we can create a ruleset with a class selector of `.heading-background`:

```css
.heading-background {
  background-color: pink;
}
```

Have a look at the [codepen](https://codepen.io/ollie-j-j/pen/xxdoWmK) example to see the background colour of the different headings change. Now pick a class in your project and use the class selector.

### ID Selector

The CSS [ID selector](https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) matches elements based on its id attribute. This can be useful to give a single element its own unique style. The ID selector differs from the class selector as it may only have a single value and be used once per page.

In the example there is a id attribute set to id `‘author-id’`. In order to select this element, we can create a ruleset with a class selector of `#author-id`:

```css
#author-id {
  color: blue;
}
```

You will notice that in the [codepen](https://codepen.io/ollie-j-j/pen/poPXLMQ) example that even though the author-class is set to red, the text has changed to blue. This is because IDs are more specific than classes so they will override any styles from a class (for the same reason classes will override any styles from a type selector).

## Advanced selectors

Now let’s move onto some more advanced selectors. You will see that selectors can unlock even more possibilities!

### Child Combinator

The [child combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator) separates two selectors and matches only those elements matched by the second selector that are direct children of elements matched by the first.

In the example, there is a list and it would be nice to add some styling to it to make it stand out. One option would be to assign a class to every `li` tag in the menu list, then write the properties for them:

In the example, there is a list and it would be nice to add some styling to it to make it stand out. One option would be to assign a class to every li tag in the menu list, then write the properties for them:

```html
<ul>
  <li class="menu-item"></li>
  <li class="menu-item"></li>
  <li class="menu-item"></li>
  <li class="menu-item"></li>
  <li class="menu-item"></li>
</ul>
```

```css
.menu-item {
  width: 100px;
  height: 50px;
}
```

However, we could use the [child combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator) to make this a bit easier. The `> combinator` will select those elements matched by the second selector that are direct children of elements matched by the first.

If we add a `menu` id to the `ul`, we can simply select all of its `li` children by using the `#menu > li` selector:

```html
<ul id="menu">
  <li>1</li>
  <li>2</li>
  <li>3</li>
  <li>4</li>
  <li>5</li>
</ul>
```

```css
#menu > li {
  width: 100px;
  height: 50px;
}
```

Now we have a rule saying that every `li` child of the element with `menu` id will have that width and height.

Now try and add a child selector to your HTML page. Here is an example in of our page [codepen](https://codepen.io/ollie-j-j/pen/GRmbdJv) if you would like to play around on that too.

### Descendant Selector

The [Descendant Selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_selectors) matches those elements **matched by the second selector**, but only those, which **have an ancestor element, matched by the first selector**.

Let's take this HTML fragment for a second and think about how we would target the `em` inside the `li`, without targeting the `em` inside the `p`:

```html
<p>Ironhack <em>Descendant</em> Selectors</p>
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li><em>item 3</em></li>
</ul>
```

```css
ul em {
  color: red
}
```

Well, we could of course add a class to the second `em`, or we could add an ID as well. However, using this combination of selectors helps us match elements without having to mess around with the HTML too much.

Here, the rule that we wrote `ul em` will apply to all `em` elements that are descendants of an `ul`. Therefore, the first `em` inside the `p` will not be affected. Useful right?

Now try and use the descendant selector in your page. Here is the descendant selector used in the [codepen](https://codepen.io/ollie-j-j/pen/MWmMGyR) example.

### Adjacent Sibling Selector

The [adjacent sibling selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_combinator) or next-sibling selector will select only the specified element that immediately follows the former specified element.

Looking at this HTML, how could we highlight the background of the fourth line?

```html
<div>
  <div>before FORMER</div>
  <div>before FORMER</div>
  <div id="former">#former</div>
  <div>next to FORMER</div>
  <div>last one...</div>
  <div>last one...</div>
</div>
```

Since it is following an id attribute, we can use the adjacent sibling selector:

```css
div {
  background-color: green;
}

#former {
 background-color: red;
}

#former + div {
  background-color: yellow;
}
```

In the [codepen](https://codepen.io/ollie-j-j/pen/OJmeZRv?editors=1100) example, see how the paragraph at the end of each section has been turned to pink using the adjacent selector.

### Multiple Selection

Imagine we want all our titles `h1`-`h6` to be colored blue. We can add a separate rule for `h1`, another rule for `h2`, another for `h3`... but there is a better way. The multiple selections allow us to apply the same list of rules to different elements:

```css
h1,
h2 {
  color: blue;
}
```

And this method can work with more complicated selectors as well, although you should probably put each selector in a different line for ease of reading. For example, we may want different elements to have background-color yellow:

```css
.todo-list > li,
h2 + .red-box,
h2 {
  background-color: yellow;
}
```

You can mix selectors as much as you need to create awesome and beautiful web pages - have a go in your project!

### Attribute Selectors

As well as selecting elements by tag name, we can also do this by its [attributes])https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors. Let’s take a look at some attributed in HTML:

```html
<a href="https://www.google.com">Google</a>
<a href="http://www.ironhack.com">Ironhack</a>
<a href="http://www.ubuntu.org">Ubuntu</a>
<a href="https://en.wikipedia.org/wiki/hacker">Wikipedia</a>
```

We can write the following CSS to change the colour of the Ironhack attribute:

```css
a[href*="ironhack"] {
  color: green;
}
a {
  display: block;
}
```

Now have a look at the [codepen](https://codepen.io/ollie-j-j/pen/eYWwrgO?editors=1100) example to see how the attributes have been changed in the page.

Here are some further examples of the attribute selector:

| Selector             | What does it select?                  |
| -------------------- | ------------------------------------- |
| `[attribute]`        | All elements with the specified attribute  |
| `[attribute=value]`  | All elements where the specified attribute is equal to ‘value’ |
| `[attribute~=value]` | All elements with an attribute which has a list of whitespace-separated values, one of which is exactly equal to ‘value’ |
| `[attribute|=value]` | All elements with an attribute which has a hyphen-separated list of values beginning (from the left) with "value" |
| `[attribute^=value]` | All elements with an attribute beginning with "value" |
| `[attribute$=value]` | All elements with an attribute ending with "value" |
| `[attribute*=value]` | All elements with an attribute containing the substring "value" |

## Experimenting with Selectors

Now you have an overview of some of the different CSS selectors, take some take to experiment with them and incorporate them into your HTML page. Use the following links to explore some new ones to add to your page too:

- [CSS Selectors - Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)
- [CSS Selectors - W3 Schools](https://www.w3schools.com/css/css_selectors.asp)
- [Interactive CSS Selectors](https://www.w3schools.com/cssref/trysel.asp)

## Exchange

Now you have an HTML page full of lots of CSS selectors you can talk them through with one of your classmates. In pairs, you should each talk through your pages and show each other which CSS Selectors you used and why.

## Reflection & Discussion

Let’s summarise what, we have covered today:

- What selectors are and why we use them.
- How to use a number of basic selectors such as type, class and id.
- How to use the Child Selector
- How to use the descendants selector
- How to combine selectors
- How to select elements based on their attribute values

Let’s discuss the following questions as a way to understand how you feel with the content from today:

- Which selectors do you feel most comfortable with?
- Which ones do you think you need to get more familiar with?
- Which selectors do you think you will need to use the most and why?

## Next Steps

### Task

Experiment and add more selectors to your page. Focus on the ones you feel least comfortable with and try some new ones out. The result doesn’t have to look beautiful, getting to grips with the selectors is the important part!

### Self Evaluation

Go to this [Miro board](https://miro.com/app/board/o9J_l13ohFs=/) and fill in the canvas to show how confident you are with CSS selectors.

### Assessment

Complete this [short quiz](https://docs.google.com/forms/d/1yprhnOKxS7Lx-Qq96VUtDNx4j5fS-W96CCQyaJsA8cA/edit) to test your knowledge on CSS selectors.

## References

- [CSS-Tricks](https://css-tricks.com/attribute-selectors/) | Interesting article explaining further uses of attribute selectors in the real world.
- [CSS Selectors](http://www.w3schools.com/cssref/css_selectors.asp) | All selectors available
- [Interactive CSS Selectors](https://www.w3schools.com/cssref/trysel.asp) | Interactive interface to play around with difference selectors
- [CSS Selectors - Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors) | All selectors
- [CSS Selectors - Overview](https://www.internetingishard.com/html-and-css/css-selectors/) | Comprehensive overview of CSS selectors
