
![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# CSS | Advanced Selectors

## Learning Goals

After this lesson, students will be able to:

- Select elements using basic selectors
- Select elements combining different selectors
- Select elements based on their relationship to other elements
- Select elements based on their attributes

## Resources: 
- Data show and notebook 
- Whiteboard or flipchart 
- Sample codes: {link to code 01 on CodePen} {link to code 02 on CodePen} 
- Youtube video about Family Tree {link to the video} 
- Quiz {link to quiz} 
- Peer2Peer feedback rubric {link to the rubrik}


## Lesson plan

Here you can find directions, guides and tools to conduct the lesson in-class. Before you start reading the lesson, let's get some tips and good practices to help you keep students engaged and connected to your class: 

- Every time you ask a question, use your audience responses to build your speech. By doing so, they will feel listened, connected and will want to participate in the class. 
- Bring your own experience to the class: They want to do the same thing you do on a daily basis. We will provide you examples and sources, but you can bring your cases to the class. 
- Apply active listening: Don't try to be the first voice in the room. Listen to your students, be empathetic and use their example to connect with your own life experiences. 
- Follow our framework for class [link for the framework]: It will help you keep the rythm to the class and build a "flow" state of mind in students. 
- Encourage debate and conversations amongst students. Make questions and motivate them to answer and comment other's answers. 
- Build opportunities for students to work in pairs or groups: Our lessons will have directions to put students working in groups sometimes. But feel free to encourage this kind of work everytime you feel it is needed. 

### Warmup

#### Learning Objective 
- Engage students in active learning, giving them a challenge where they will try to solve the problem they will work on the lesson. 

#### Suggested timekeeping: 
10 ~ 15 minutes

#### Description
The first part of the class, after presentations and welcoming, needs to be the explanation of the Agenda. You can wrote on the flipchart/whiteboard and explain students what is going to happen. After that, you can explain the challenge for students. They will have a sample code with some directions to style the code accordingly. Consider they know the basics of HTML and CSS, so the task will be to optimize their work in this kind of task. 

#### Steps for conducting the class 
- Clarify the agenda of the class for students:
- - Mention the topics of the lesson and how will it be conducted. 
- - Mention an estimate of time that will be spent in each part of the lesson
- - Make agreements with the class: How are the questions being asked? Will there be breaks? What about the agreements with the notebooks? Feel free to design your own agreements. 
- - Mention what will be the assessments: They will have a quiz and a peer-to-peer activity.
- Ask students to open their lessons in their own notebooks. 
- Use the data show to share the code 01 and analyze it with the students. 
- Explain the challenge: They will need to try to follow the directions given in the lesson using their previous knowledge. 
- Give them 10 minutes to try to figure out how to work on the directions. 

The focus here is not to reach the full resolution of the challenge. The idea is to engage students and make them curious about what you are going to teach them. Here, we are starting with the "why", which means we are showing them what problem this lesson will help them to solve. 

During this 10 minutes, walk around the class, check what students are doing, aswer questions when they can be quickly answered. Try to be aware of what are the main painpoints of the students. 

- By the end of the time, ask for some voices to show you how they would solve the problem. **Don't give answers yet, the goal here is to make them curious and challenged.** Ask if someone would think of different ways to follow the instructions.
- End this part by explaining the main goal of this lesson, which is to learn some tools to help optimizing the task of styling HTML codes using CSS Combining Selectors. 

### Intro 

#### Learning Objective 
- Identify the main characteristics of a Family Tree inside a HTML code, based on the Document Object Model approach.

#### Suggested timekeeping 
20 minutes 

#### Description
Explain that before learning about Combining CSS Selectors, it is important to understand the Document Tree in the Document Object Model. The main goal here is to relate a regular family tree to a HTML diagram and identify its relevance to combining selectors. 

#### Steps for conducting the class 
- Go back to the image of the code 01
- Try to provoke students to find relations between the tags 
- You can ask questions, like "which tags would be the parents?" "and which would be its siblings or descendants?" 
- Use the whiteboard or flipchart to draw a family-tree like structure. Take notes on students answers. 
- Explain the concept of the Document Object Model. 
- You can use the video to visually facilitate the organization of the code in a tree or you can draw it by yourself and explain as you draw the relations. 
- After this, finish this part of the lesson by defining the relations of the tags in the code. You don't need to show them all, since they will be described during the lesson, but give some examples to materialize the concept. 

## Combining CSS Selectors 

### Selecting Direct Descendants (Children)

#### Learning Objective
Define the Children Selector, its syntaxis and proper application through the analysis and practice on a real example. 

#### Suggested timekeeping 
15 minutes 

#### Description
The following topics (Direct Descendants, Descendant Selectors and Adjacent Siblings) will work on the same code you used in the beginning of the lesson. Likewise, the tasks that will be developed will be the same as students tried to solve in the warmup. The goal here is to crack that challenge and smaller pieces and show the application of each selector related to each task. 

#### Steps to conduct the class 
- Go back to the first task of the lesson: 
**Style all the `li` tags inside the menu `ul` with size of **50px height and 100px width****

- Ask for the students to answer which would be one option to solve this. Explain that one option to solve the task would be to assign a class to every `li` tag in the menu list, then write the properties for them:

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

- Comment the amout of work this would give and explain the concept and syntaxis of the Child Selector, using the text of the lesson (of course, feel free to explain it on your own way)
- Show them how to use the child selector to add a menu to the `ul`. 

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
- Explain the use of rules and how they work together with the selectors, relating that to the family tree. 

#### Descendant Selectors

#### Learning Objective 
Define the Descendant Selector, its syntaxis and proper application through the analysis and practice on a real example. 

#### Suggested timekeeping
15 minutes

#### Description 
Continuing on the work with the same code you used in the beginning of the lesson, the goal with this topic is to solve the following task: 
**- Style **just** the `em` inside the `ul` in **red**.**

#### Steps to conduct the class 
- Go back to the related task. 
- Ask students how did they solve this task in the beginning of the class. Explain that one option would be to add a class to the second **`em`**, or we could add an ID as well. 

![](https://i.imgur.com/YdqDUNh.png)

- Explain that the application of Descendant Selectors helps us match elements without having to mess around with the HTML too much.
- Guide students in doing so in the sample code. 

 ```html
<p>Ironhack <em>Descendant</em> Selectors</p>
<ul>
  <li>item 1</li>
  <li>item 2</li>
  <li><em>item 3</em></li>
</ul>
```
- Question students about how different it is to use the solutions they found in the beginning of the lesson. 
- Talk about how important it is to keep the code clean and compact. 

### Selecting Siblings 

#### Adjacent Siblings

#### Learning objective
Define the Descendant Selector, its syntaxis and proper application through the analysis and practice on a real example. 

#### Suggested timekeeping 
15 minutes 

#### Description
As this topic is a little more complicated, we will start with a different example, to summarize how this selector allows you to get elements that are next to each oter. You can comment this code regarding how are the selected elements related to each other and then continue to the code used on the beginning of the lesson. 

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Print+of+an+example+appears+here) 

[// Here we would have a print with a code, which could be something like this https://codepen.io/thaisgellert/pen/GRmGyvB, with the image of the css code below with comments just as the original lesson//]: #

- After you analized the example, the goal with this topic is to solve the following task: 
**- Style all the `div` tags with a **green background**, but the `div` on line 4 with a **red background**, and the one in the next line with a **yellow background**.**

#### Steps to conduct the class
- Go back to the code you were working on the beginning of the class
- Ask students how they solved the task using their own knowledge. 
- Make comments about their answers and check to understand if everyone is following your lead. You can ask for particular students to share their answers. This doesn't aim at exposing anyone: Please remember that the class is a safe space and this is the time for them to try, make mistakes and guesses. 
- Explain that to use the Adjacent Sibling selector, they need to define which will be the FORMER tag, because it is from this tag that the others will be styled.
- Show them the application of the selector: 

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
- Check if students have questions, go around the class and check if students are doing the activities in their own notebooks. Give feedback, pay attention to those that may be facing more difficult times in understanding this activity. 

- Remember students that the one of the goals of this course is to teach you them keep the HTML as tidy, clean, and compact as possible. These selectors will help you target elements without having to add classes everywhere. 

### Exercise: Quiz 

#### Learning objective 
Assess learning to determine successful learning of the previous content. 

#### Suggested Timekeeping
30 minutes

#### Description: TBD
[// Here we put a quiz that can be developed at https://landbot.io/, where we build a chatbot to check the understanding of the concepts and processes to this part of the lesson. Depending on the strategy we decide to follow we can work both with case-based quizzes - the same as the lesson - to develop processual thinking or with conceptual questions, to check the knowledge on a conceptual level//]: #

#### Steps to conduct the activity 
- Explain students that before continuing the lesson, they will answer a quick quiz to check how they are going until this part. 
- Ask them if they have any questions before starting the quiz 
- Use the credentials we gave you to the chatbot so you can follow their answers 
- Ask students to correctly fill their names for the activity, so you can follow their answers. 
- While they are working on the activity, follow the results and take notes on the students that may be striving and those who are thriving. 
- After the end of the activity, if you feel the need, you can make them work in pairs or groups, balancing the levels of students so they can support each other.
- Give feedback, pay attention to the main pain points and, if needed, take some time to go back to the topic that is concerning the students. 

### Warmup

#### Learning Objective
- Engage students in active learning, giving them a challenge where they will try to solve the problem they will work on the lesson. 

#### Suggested timekeeping
10 minutes

#### Description
In the same way they did in the first part of the class, this time they will have a different code so they can try to style following directions. Explain that to them, recall the Agenda you've shown in the beginning of the class and explain the challenge for students. 

#### Steps for conducting the class
- Check if students are in the right part of the lesson in their notebooks.
- Use the data show to share the code 02 and analyze that with students. 
- Explain the challenge: They will need to try to follow the directions given in the lesson using their previous knowledge. Give them 10 minutes to try to figure out how to work on the directions.
- Give them 10 minutes to try to figure out how to work on the directions.

During this 10 minutes, walk around the class, check what students are doing, aswer questions when they can be quickly answered. Try to be aware of what are the main painpoints of the students.

By the end of the time, ask for some voices to show you how they would solve the problem. Don’t give answers yet, the goal here is to make them curious and challenged. Ask if someone would think of different ways to follow the instructions.
End this part by explaining the main goal of this lesson, which is to learn some tools to help optimizing the task of styling HTML codes using CSS Combining Selectors.

### Multiple Selectors

#### Learning Objective
Define the Multiple Selectors, its syntaxis and proper application through the analysis and practice on a real example. 

#### Description
In this part of the class, students will work on a different code. Given that you have Code 02 {link}, the goal of this topic is to solve the following task: 
**- Style all the titles in **blue****

#### Steps to conduct the class 
- Ask students how would they follow this direction. 
- Explain that one option would be the addition of a separate rule for `h1`, another rule for `h2`, another for `h3` and so one until listing all the titles.
- Ask for their opinion: Would it make sense? Is there anything wrong with this solution? 
- Explain that it would bring a lot of work and make the code longer and heavier, we have a better way: **The multiple selections allow us to apply the same list of rules to different elements**. 

```css
h1,
h2 {
  color: blue;
}
```
- Tell them that this method can work with more complicated selectors as well, although you should probably put each selector in a different line for ease of reading. For example, we may want different elements to have background-colour yellow:

```css
.todo-list > li,
h2 + .red-box,
h2 {
  background-color: yellow;
}
```

- Discuss other examples with the class, try to motivate them to play around with the code to understand that they can mix selectors as much as they want to create the pages according to their creativity. 

#### Attribute selector 

#### Learning Objective
Define the Attribute Selectors, its syntaxis and proper application through the analysis and practice on a real example. 