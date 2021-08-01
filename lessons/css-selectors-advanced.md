![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# CSS | Advanced Selectors

## Learning Goals

After this lesson, you will be able to:

- Select elements using basic selectors
- Select elements combining different selectors
- Select elements based on their relationship to other elements
- Select elements based on their attributes

## Intro

Before learning about combined CSS selectors, it's a good idea to understand the document tree in the **Document Object Model**. If you understand the document tree concept, then CSS selectors will be much easier to understand and therefore apply.

The Document Object Model (DOM) is a cross-platform and language-independent interface that treats an XML or HTML document as a tree structure wherein each node is an object representing a part of the document. The DOM represents a document with a logical tree. Each branch of the tree ends in a node, and each node contains objects

All HTML documents can be represented as trees. Each level of the tree is described in the same manner as a human family tree, with ancestors, descendants, parents, children and siblings. CSS selectors can describe elements in the document tree. 

In the following video you can check a visual facilitation to help you understand the concepts and relation between the members of a family tree.

[// Below you have a sample a video I made to visually facilitate the concepts of the Family Tree and its components//]: #

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/5JkT3E56JPI" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

[// The idea of this exercise is to fix the concepts and to relate the content to the video. In the case of a in-class experience, the instructor could ask to students to answer the questions; otherwise in order to be remote-friendly, this can be done with an interactive activity //]: #

Now, getting back to the code seen in the video, let's solve a quick exercise: 

![Family Tree Example](https://i.imgur.com/iU8qaV4.jpg) 


* Name the children of the tag <body>
* How is the tag <aside> related to <selection>? 
* How are the <li> tags related to <aside>? 
* Name three other relation between the tags. 

## CSS Selectors: Review
[// This is a proposal for a quick review, recalling some previous content seen in other lessons, necessary to scaffold this theme. As this is an exemple, all of this information came from https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks//]: #

In the previous lessons you got familiar ith the CSS Selectors. You are aware that there are a lot of CSS selectors available, allowing for fine-grained precision when selecting elements to style. In case you want to recap those lessons, you can click on the following links to acess previous content: 

* [Type, class and ID Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors)
* [Attribute Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors)  
* [Pseudo-classes and pseudo-elements](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)

Now, in this lesson, we will talk about the last type of selector, the Combinators.

[// I added some information to the existing content, in order to remove all of the external links and give more fundamentals on each topic. All of the information were recalled from https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators//]: #

## Combining CSS Selectors 

### Selecting Descendants

#### Child Selectors

```css
parent > child {
  property: value;
}
```

Typically represented as the “is more than” signal (>), the Child Combinator separates two selectors and matches only those elements matched by the second selector that are direct children of elements matched by the first. Elements matched by the second selector must be the immediate children of the elements matched by the first selector. 

Imagine you have several lists and you want to style them all. All `li` tags inside the menu `ul` tag will have **50px height and 100px width**. One option would be to assign a class to every `li` tag in the menu list, then write the properties for them:

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

This would give a lot of work, since a full website has a lot of tags, right? Then, we have a much easier way. **The child selector** will select those elements matched by the second selector that are direct children of elements matched by the first.

If we add a `menu` id to the `ul`, we can simply select all of its `li` children by using the **`#menu > li`** selector:

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

Now we have a rule saying that **every `li` child of the element with `menu` id will have that width and height**.

Now you are familiar with the Child Selectors, let's play around: 
In the CSS box, try to change the color of all **`p`** elements, that are immediate children of **`div`** elements, to **"red"**. You can use your imagination and practice as much as you want to! 

Warning
:zap: Remember to click **Edit on CodePen** so you can code along and play around

[// Here I browsed a child combinator exercise on codePen, and this is recalled from https://codepen.io/ewusiessel/pen/Pobdjwr //]: #

<iframe height="300" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/ewusiessel/embed/Pobdjwr?default-tab=html%2Cresult&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/ewusiessel/pen/Pobdjwr">
  child combinator selectors</a> by ewusiessel (<a href="https://codepen.io/ewusiessel">@ewusiessel</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

#### Descendant Selector

``` css 
selector1 selector2 {
  property: value;
}
```
Typically represented by a single space ( ) character — the descendant selector matches those elements **matched by the second selector**, but only those, which **have an ancestor element, matched by the first selector**. Selectors that utilize a descendant combinator are called descendant selectors.

The descendant combinator is technically one or more CSS white space characters — the space character and/or one of four control characters: carriage return, form feed, new line, and tab characters — between two selectors in the absence of another combinator. Additionally, the white space characters of which the combinator is comprised may contain any number of CSS comments.

Let's take this HTML fragment for a second and think about how we would target the **`em`** inside the **`li`**, without targeting the **`em`** inside the **`p`**:

```html
<p>Ironhack <em>Descendant</em> Selectors</p>
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li><em>item 3</em></li>
</ul>
```

Well, we could of course add a class to the second **`em`**, or we could add an ID as well. However, using this combination of selectors helps us match elements without having to mess around with the HTML too much.

![](https://i.imgur.com/YdqDUNh.png)

One of the goals of this course is to teach you to keep the HTML as tidy, clean, and compact as possible. These selectors will help you target elements without having to add classes everywhere. 

Now that you are familiar with Descendant Selectors, let's get some practice: Here, the rule that we wrote **`ul em`** will apply to all **`em`** elements that are descendants of an **`ul`**. Therefore, the first **`em`** inside the **`p`** will not be affected.

**Warning**
:zap: Remember to click **Edit on CodePen** so you can code along and play around
 

<iframe height="300" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/ironhack/embed/amBQkV?default-tab=html%2Cresult&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/ironhack/pen/amBQkV">
  </a> by Ironhack (<a href="https://codepen.io/ironhack">@ironhack</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

Useful, right?

### Select Siblings

#### Adjacent Siblings 

The Adjacent Selector or next-sibling selector is tipically represented as the "plus" sign (+) and will select only the specified element that immediately follows the former specified element. As you can see in the example, this selector allows you to get elements that are next to each other:

<iframe height='265' scrolling='no' src='//codepen.io/ironhack/embed/amBQEG/?height=265&theme-id=light&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/ironhack/pen/amBQEG/'>Example</a> by Ironhack (<a href='http://codepen.io/ironhack'>@ironhack</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

If we look carefully at the CSS code, these standards can be noticed:

* All DIVs are green for default:
```css
div {
  background-color: green;
}
```
* We have the ID for the **former** divider and are making it red. 
```css
#former {
  background-color: red;
}
``` 
* And have the first adjacent sibiling of **#former** to be yellow. 
```css
#former + div {
  background-color: yellow;
}
```

Now this is getting a little more complex, what about some more exercises? Going back to CodePen, try to change the colors and style for some random lines in the following example: 

**Warning**
:zap: Remember to click **Edit on CodePen** so you can code along and play around

<iframe height="300" style="width: 100%;" scrolling="no" title="" src="https://codepen.io/thaisgellert/embed/GRmGyvB?default-tab=html%2Cresult&editable=true" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/thaisgellert/pen/GRmGyvB">
  </a> by thaisgellert (<a href="https://codepen.io/thaisgellert">@thaisgellert</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>

### Multiple selection

```css
selector1,
selector2 {
  property: value;
}
```

Imagine we want all our titles `h1`-`h6` to be colored blue. We can add a separate rule for `h1`, another rule for `h2`, another for `h3`... As it would also bring a lot of work and make the code longer and heavier, we have a better way: **The multiple selections allow us to apply the same list of rules to different elements**. 

```css
h1,
h2 {
  color: blue;
}
```

This method can work with more complicated selectors as well, although you should probably put each selector in a different line for ease of reading. For example, we may want different elements to have background-color yellow:

```css
.todo-list > li,
h2 + .red-box,
h2 {
  background-color: yellow;
}
```

You can mix selectors as much as you need to create awesome and beautiful web pages!

### Attribute Selector

```css
element[attr-name="value"] {
  property: value;
}
```

For the times we need to select more elements, besides the selection by the tag name as you've seen above, we can also select them by their attributes. To define an attribute for an element, you need to put them between `[]` and give them a name. 

In the following example, only the links with the word hack in their src attribute are affected by the rule, and therefore are show in green.

```css
a[href*="hack"] {
  color: green;
}
a {
  display: block;
}
```

<iframe height='265' scrolling='no' src='//codepen.io/ironhack/embed/GjAWAo/?height=265&theme-id=light&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/ironhack/pen/GjAWAo/'>GjAWAo</a> by Ironhack (<a href='http://codepen.io/ironhack'>@ironhack</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

Another examples of this same selector:

| Selector             | What does it select?                  |
| -------------------- | ------------------------------------- | 
| `[attribute]`        | All elements with the specified attribute  |
| `[attribute=value]`  | All elements where the specified attribute is equal to ‘value’ |
| `[attribute~=value]` | All elements with an attribute which has a list of whitespace-separated values, one of which is exactly equal to ‘value’ |
| `[attribute|=value]` | All elements with an attribute which has a hyphen-separated list of values beginning (from the left) with "value" |
| `[attribute^=value]` | All elements with an attribute beginning with "value" |
| `[attribute$=value]` | All elements with an attribute ending with "value" |
| `[attribute*=value]` | All elements with an attribute containing the substring "value" |

Here you have one more example to play around:

<iframe height="485" style="width: 100%;" scrolling="no" title="attr-selectors-css" src="https://codepen.io/abernier/embed/NWKmera?height=485&theme-id=0&default-tab=html,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/abernier/pen/NWKmera'>attr-selectors-css</a> by Antoine BERNIER
  (<a href='https://codepen.io/abernier'>@abernier</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## Summary

In this lesson, you have learnt:

- How to select descendants `selector1 selector2` and children `selector1 > select2` of a node
- How to select siblings `selector1 + selector2` of a node
- How to combine selector rules `selector1, selector2`
- How to select elements based on their attribute values `element[attr="value"]`

## Extra Resources

- [Css-tricks](https://css-tricks.com/attribute-selectors/) | Interesting article explaining further uses of attribute selectors in the real world.
- [CSS Selectors](http://www.w3schools.com/cssref/css_selectors.asp) | All selectors available
