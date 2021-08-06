
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# CSS | Advanced Selectors

## Learning Goals

After this lesson, you will be able to:

- Select elements using basic selectors
- Select elements combining different selectors
- Select elements based on their relationship to other elements
- Select elements based on their attributes

## Warmup 

Now that you are familiar with the basics of HTML and CSS, let's take this code as an example and try to style it according to the following instructions: 

[// Here the idea is to give an example code, that will be used through the first part of the lesson. The main goal is to start the topic with a challenge, let students try to figure it out on their own and then break the code into parts so they are "finding" the answers for their doubts during the lesson //]: #

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

- Style all the `li` tags inside the menu `ul` with size of **50px height and 100px width**.
- Style **just** the `em` inside the `ul` in **red**. 
- Style all the `div` tags with a **green background**, but the `div` on the line 4 with a **red background**, and the one in the next line with a **yellow background**. 

Challenging, right? Give style to a website can be quite a laborious task, but in this lesson, you will learn some tools that can optimize your work on this job. 

## Intro

Before learning about combined CSS selectors, it's a good idea to understand the document tree in the **Document Object Model**. If you understand the document tree concept, then CSS selectors will be much easier to understand and therefore apply.

Let's go back to the previous code: 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Print+of+the+code+appears+here)

Try to analyze it and understand how each tag is related to the others, considering it as a family tree. Which tags would be the parents? Which ones would be the children or the siblings? Now try to draw on your notebook some kinship between the tags, using a family tree logic: 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=A+regular+family+tree+diagram+appears+here)

The Document Object Model (DOM) is an interface that treats an XML or HTML documents as a tree structure wherein each node is an object representing a part of the document. The DOM represents a document with a logical tree. Each branch of the tree ends in a node, and each node contains objects

All HTML documents can be represented as trees. Each level of the tree is described in the same manner as a human family tree, with ancestors, descendants, parents, children and siblings. CSS selectors can describe elements in the document tree. 

In the following video, you can check visual facilitation to help you understand the concepts and relations between the members of a family tree.

[// Below you have a prototype of a video I made to visually facilitate the concepts of the Family Tree and its components//]: #

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/5JkT3E56JPI" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

After you watched the video, go back to your notes and check how you did in the description of the relationship between the tags in the code.

## Combining CSS Selectors

### Selecting Descendants

#### Direct Descendants (Children)

```css
parent > child {
  property: value;
}
```

Typically represented as the “is more than” signal (>), the Child Combinator separates two selectors and matches only those elements matched by the second selector that are direct children of elements matched by the first. Elements matched by the second selector must be the immediate children of the elements matched by the first selector. 

Now let's go back to the first task you found in this lesson: 
- Style all the `li` tags inside the menu `ul` with size of **50px height and 100px width**.

One option to solve the task would be to assign a class to every `li` tag in the menu list, then write the properties for them:

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

This would give a lot of work since a full website has a lot of tags, right? Then, we have a much easier way. **The child selector** will select those elements matched by the second selector that are direct children of elements matched by the first.

No let's re-do this on our previous code: Add a `menu` id to the `ul`, we can simply select all of its `li` children by using the **`#menu > li`** selector:

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

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

#### Descendant Selector

``` css 
selector1 selector2 {
  property: value;
}
```

Typically represented by a single space ( ) character — the descendant selector matches those elements **matched by the second selector**, but only those, which **have an ancestor element, matched by the first selector**. Selectors that utilize a descendant combinator are called descendant selectors.

The descendant combinator is technically one or more CSS white space characters — the space character and/or one of four control characters: carriage return, form feed, new line, and tab characters — between two selectors in the absence of another combinator. Additionally, the white space characters of which the combinator is comprised may contain any number of CSS comments.

Now let's go back to the code and the task you had at the beginning of the lesson:
- Style **just** the `em` inside the `ul` in **red**. 

Think about how we would target the **`em`** inside the **`li`**, without targeting the **`em`** inside the **`p`**. We could of course add a class to the second **`em`**, or we could add an ID as well. 

![](https://i.imgur.com/YdqDUNh.png)

However, using this combination of selectors helps us match elements without having to mess around with the HTML too much. So let's do this in our code: Write the rule **`ul em`**, which will apply to all **`em`** elements that are descendants of an **`ul`**. Therefore, the first **`em`** inside the **`p`** will not be affected.

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

```html
<p>Ironhack <em>Descendant</em> Selectors</p>
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li><em>item 3</em></li>
</ul>
```
Useful, right?

### Select Siblings

#### Adjacent Siblings 

The Adjacent Selector or next-sibling selector is typically represented as the "plus" sign (+) and will select only the specified element that immediately follows the former specified element. Now, this is getting a little more complicated, let's check an example before going to practice. 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Print+of+an+example+appears+here)

As you can see in the example, this selector allows you to get elements that are next to each other. If we look carefully at the CSS code, these standards can be noticed:

[//Here I will work with a different example to keep the example of the lesson, could be something like this: https://codepen.io/thaisgellert/pen/GRmGyvB, but unfortunately I don't know how to make this analysis]:#

```css
{example of the analysis of the code
} 
with comments
```

Now you got familiar with the concept, let's go back to your task at the beginning of the lesson: 

- Style all the `div` tags with a **green background**, but the `div` on line 4 with a **red background**, and the one in the next line with a **yellow background**. 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

So to apply the **Adjacent Sibling Selector**, we would do the following: 

Give the ID "FORMER" to the `div` in line 4
Style all `div`as green by default: 
```css
div {
background-color: green;
}
```

Make the `div`with the ID = FORMER red
```css
#former {
    background-color: red;
}
```

Use the selector to make the first adjacent sibling of #FORMER yellow
```css
+former + div {
    background-color: yellow;
} 
```

So, what do you think? One of the goals of this course is to teach you to keep the HTML as tidy, clean, and compact as possible. These selectors will help you target elements without having to add classes everywhere. 

Before going further on the lesson, let's work through a quick quiz to check your evolution until this part: 

## Exercise: Quiz. 

[// Here we put a quiz that can be developed at https://landbot.io/, where we build a chatbot to check the understanding of the concepts and processes to this part of the lesson. Depending on the strategy we decide to follow we can work both with case-based quizzes - the same as the lesson - to develop processual thinking or with conceptual questions, to check the knowledge on a conceptual level//]: #

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Chatbot+with+quiz+appears+here)

## Warmup 

Now that you are familiar with the Combinators, you will know some tools to help you work with more than one selector and have an even cleaner code. 

[// Here the idea is to give an example code, that will be used through the second part of the lesson. The main goal is to start the topic with a challenge, let students try to figure it out on their own and then break the code into parts so they are "finding" the answers for their doubts during the lesson //]: #

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

- Style all the titles in **blue**
- Style all the links with the word "hack" in their src in **green**.

### Multiple selection
```css
selector1,
selector2 {
  property: value;
}
```

Now let's go back to your first task: 
- Style all the titles in **blue**

One solution could be the addition of a separate rule for `h1`, another rule for `h2`, another for `h3`... As it would bring a lot of work and make the code longer and heavier, we have a better way: **The multiple selections allow us to apply the same list of rules to different elements**. 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

```css
h1,
h2 {
  color: blue;
}
```

This method can work with more complicated selectors as well, although you should probably put each selector in a different line for ease of reading. For example, we may want different elements to have background-colour yellow:

```css
.todo-list > li,
h2 + .red-box,
h2 {
  background-color: yellow;
}
```

You can mix selectors as much as you need to create awesome and beautiful web pages! Feel free to play along with the example code and see where your creativity will take you! 

### Attribute Selector

```css
element[attr-name="value"] {
  property: value;
}
```

Going back to your second task: 
- Style all the links with the word "hack" in their src in **green**.

If we can select elements by tag name, why not select an element by its attributes?
For the times we need to select more elements, we can also select them by their attributes. To define an attribute for an element, you need to put them between `[]` and give them a name. 

In the following example, only the links with the word hack in their src attribute are affected by the rule and therefore are shown in green. Now let's do that in our example code: 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

```css
a[href*="hack"] {
  color: green;
}
a {
  display: block;
}
```

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

## Exercise: Peer review. 

Now that you are familiar with these two selectors, what about creating your own style for this example and submit your code for peer-reviewing? Once you submit your code, you will receive a guide to review your peer's codes as well! 

[// Here we could add a link where students can submit their codes and, once they submit their activities, they receive a little rubric where they can evaluate other peer's codes as well.//]:#

## Summary

In this lesson, you have learnt that: 

- HTML documents are represented as family trees and it is the fundamental base of the Document Object Model (DOM) 
- Child selector is represented by the (>) signal and is used to select direct descendants to style. 
- Descendant selector is represented by blank spaces (  ) and is used to select elements matched by the second selector, but only those which have an ancestor element matched by the first selector. 
- Adjacent Selector is represented by the (+) signal and is used to select only the specific element that immediately follows the former specified element. 
- We can use multiple selections to apply the same list of rules to different elements, selecting by tag names or attributes. 

## Extra Resources

- [Css-tricks](https://css-tricks.com/attribute-selectors/) | Interesting article explaining further uses of attribute selectors in the real world.
- [CSS Selectors](http://www.w3schools.com/cssref/css_selectors.asp) | All selectors available
- [Document Object Model](https://www.w3.org/TR/WD-DOM/introduction.html) | More detailed information about the Document Object Model API. 
