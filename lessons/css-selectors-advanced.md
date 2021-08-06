![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

[// The goal of this learning plan is to support instructors in the application of the lesson in a student-face environment. To support this instructor, we would need to provide some resources as the class framework, which proposal I will be sharing during my presentation, 3 code examples and the tools for assessment: the chatbot quiz and the structure for a peer to peer evaluation, that can be developed but I might need to better understand the technology we would have to do such kind of activity. The proposal of the lesson is to replicate the experience of students in the lesson, but where we have the embedded codes in the lesson, we will have the instructor screen sharing and explaining the resolution of the tasks on the go.//]: # 

# CSS | Advanced Selectors

## Learning Goals
### After this lesson, students will be able to:
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
Here you can find directions, guides and tools to conduct the lesson in class. Before you start reading the lesson, let’s get some tips and good practices to help you keep students engaged and connected to your class:
- Every time you ask a question, use your audience responses to build your speech. By doing so, they will feel listened to, connected and will want to participate in the class.
- Bring your own experience to the class: They want to do the same thing you do on a daily basis. We will provide you with examples and sources, but you can bring your cases to the class.
- Apply active listening: Don’t try to be the first voice in the room. Listen to your students, be empathetic and use their example to connect with your own life experiences.
- Follow our framework for class [link for the framework]: It will help you keep the rhythm to the class and build a “flow” state of mind in students.
- Encourage debate and conversations amongst students. Make questions and motivate them to answer and comment on other’s answers.
- Build opportunities for students to work in pairs or groups: Our lessons will have directions to put students working in groups sometimes. But feel free to encourage this kind of work every time you feel it is needed.

## Onboarding
The first part of the class, after presentations and welcoming, needs to be the explanation of the Agenda. You can write on the flipchart/whiteboard and explain to students what is going to happen.

Clarify the agenda of the class for students:
- The topics of the lesson and how will it be conducted.
- An estimate of the time that will be spent in each part of the lesson
- Make agreements with the class: How are the questions being asked? Will there be breaks? What about the agreements with the notebooks? Feel free to design your own agreements.
- There will be assessments: They will have a quiz and a peer-to-peer activity.
- Ask students to open their lessons in their own notebooks.

## Warmup

### Learning Objective
Engage students in active learning, giving them a challenge where they will try to solve the problem they will work on in the lesson.
### Suggested timekeeping:
10 ~ 15 minutes
### Description
Explain the challenge: They will need to follow the directions given in the lesson using their previous knowledge.Consider they know the basics of HTML and CSS, so the challenge will be to optimize their work in this kind of task using Combining Selectors.

### Steps for conducting the class

- Use the data show to share code 01 and analyze it with the students.
- Explain the challenge: 

[// Here the idea is to give an example code, that will be used through the first part of the lesson. The main goal is to start the topic with a challenge, let students try to figure it out on their own and then break the code into parts so they are "finding" the answers for their doubts during the lesson //]: #

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Embedded+Code+Appears+Here)

- Style all the `li` tags inside the menu `ul` with size of **50px height and 100px width**.
- Style **just** the `em` inside the `ul` in **red**. 
- Style all the `div` tags with a **green background**, but the `div` on the line 4 with a **red background**, and the one in the next line with a **yellow background**. 
- End this part by explaining the main goal of this lesson, which is to learn some tools to help to optimize the task of styling HTML codes using CSS Combining Selectors.

The focus here is not to reach the full resolution of the challenge. The idea is to engage students and make them curious about what you are going to teach them. Here, we are starting with the "why", which means we are showing them what problem this lesson will help them to solve. 

During this 10 minutes, walk around the class, check what students are doing, aswer questions when they can be quickly answered. Try to be aware of what are the main painpoints of the students. 

- By the end of the time, ask for some voices to show you how they would solve the problem. **Don't give answers yet, the goal here is to make them curious and challenged.** Ask if someone would think of different ways to follow the instructions.
- End this part by explaining the main goal of this lesson, which is to learn some tools to help optimizing the task of styling HTML codes using CSS Combining Selectors. 

## Intro
### Learning Objective
Identify the main characteristics of a Family Tree inside an HTML code, based on the Document Object Model approach.
### Suggested timekeeping
20 minutes
### Description
Explain that before learning about Combining CSS Selectors, it is important to understand the Document Tree in the Document Object Model. The main goal here is to relate a regular family tree to an HTML diagram and identify its relevance to combining selectors.
### Steps for conducting the class
- Go back to Code 01 
- Ask students to find relations between the tags
- You can ask questions, like “which tags would be the parents?” “and which would be its siblings or descendants?”
- Use the whiteboard or flipchart to draw a family-tree like structure. Take notes on students answers.
- Explain the concept of the Document Object Model. You can use the video to visually facilitate the organization of the code in a tree or you can draw it by yourself and explain as you draw the relations.
- After this, finish this part of the lesson by defining the relations of the tags in the code. You don’t need to show them all since they will be described during the lesson, but give some examples to materialize the concept.

## Combining CSS Selectors
### Selecting Direct Descendants (Children)

### Learning Objective
Define the Children Selector, its syntaxis and proper application through the analysis and practise on a real example.
### Suggested timekeeping
15 minutes
### Description
The following topics (Direct Descendants, Descendant Selectors and Adjacent Siblings) will work on the same code you used at the beginning of the lesson. Likewise, the tasks that will be developed will be the same as students tried to solve in the warmup. The goal here is to crack that challenge into smaller pieces and show the application of each selector related to each task.
### Steps to conduct the class
- Go back to the first task of the lesson: **Style all the li tags inside the menu ul with a size of 50px height and 100px width**
- Ask for the students to answer which would be the options to solve this, what did they do at the beginning of the class. Explain that one option to solve the task would be to assign a class to every `li` tag in the menu list, then write the properties for them:
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
- Mention the amount of work this would give and explain the concept and syntaxis of the Child Selector, using the text of the lesson *(of course, feel free to explain it in your own way)*.
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

## Descendant Selectors
### Learning Objective
Define the Descendant Selector, its syntaxis and proper application through the analysis and practise on a real example.
### Suggested timekeeping
15 minutes
### Description
Continuing on the work with the same code you used at the beginning of the lesson, the goal with this topic is to solve the following task: **Style just the `em` inside the `ul` in red.**
### Steps to conduct the class
- Go back to the related task.
- Ask students how did they solve this task at the beginning of the class. Explain that one option would be to add a class to the second `em`, or we could add an ID as well.
-![](https://i.imgur.com/YdqDUNh.png)
- Explain that the application of Descendant Selectors helps us match elements without having to mess around with the HTML too much.
- Guide students in doing so in the sample code.
```html
<p>Ironhack <em>Descendant</em> Selectors</p>
<ul>
 <li>item 1</li>
 <li>item 2</li>
 <li><em>item 3</em></li>
</ul
```
- Question students about how different it is to use the solutions they found at the beginning of the lesson.
- Talk about how important it is to keep the code clean and compact.

## Selecting Siblings
### Adjacent Siblings
### Learning objective
Define the Descendant Selector, its syntaxis and proper application through the analysis and practise on a real example.
### Suggested timekeeping
15 minutes
### Description
As this topic is a little more complicated, we will start with a different example, to summarize how this selector allows you to get elements that are next to each other. You can comment on this code regarding how are the selected elements related to each other and then continue to the code used at the beginning of the lesson.

![PlaceHolder](https://via.placeholder.com/450x300.png?text=Print+of+an+example+appears+here) 

[// Here we would have a print with a code, which could be something like this https://codepen.io/thaisgellert/pen/GRmGyvB, with the image of the css code below with comments just as the original lesson//]: #

- After you analyzed the example, the goal with this topic is to solve the following task: **Style all the `div` tags with a green background, but the `div` on line 4 with a red background, and the one in the next line with a yellow background.** 
### Steps to conduct the class
- Go back to the code you were working on at the beginning of the class
- Ask students how they solved the task using their own knowledge.
- Make comments about their answers and check to understand if everyone is following your lead. You can ask particular students to share their answers. This doesn’t aim at exposing anyone: Please remember that the class is a safe space and this is the time for them to try, make mistakes and guesses.
- Explain that to use the Adjacent Sibling selector, they need to define which will be the FORMER tag, because it is from this tag that the others will be styled.
- Guide them to do the application of the selector:

Give the ID “FORMER” to the div in line 4
Style all divas green by default:
```css
div {
background-color: green;
}
```
Make the div with the ID = FORMER red
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
- Remember students that one of the goals of this course is to teach them to keep the HTML as tidy, clean, and compact as possible. These selectors will help them target elements without having to add classes everywhere.

## Exercise: Quiz
### Learning objective
Assess learning to determine successful learning of the previous content.
### Suggested Timekeeping
30 minutes
### Description: 
[// The main characteristics of the quiz would depend on the type of activity we would decide to do, this is why it is "to be defined" here//]: # 

### Steps to conduct the activity
[// If we use the tool landbot.io, we could create a chatbot with the quiz with general credentials that will be shared with the instructor in the lesson so they can follow the student's ansewrs on the assessment.//]: # 
- Explain to students that before continuing the lesson, they will answer a quick quiz to check how they are going until this part.
- Ask them if they have any questions before starting the quiz
- Use the credentials we gave you to the chatbot so you can follow their answers.
- Ask students to correctly fill their names for the activity, so you can follow their answers.
- While they are working on the activity, follow the results and take notes on the students that may be striving and those who are thriving.
- After the end of the activity, if you feel the need, you can make them work in pairs or groups, balancing the levels of students so they can support each other.
- Give feedback, pay attention to the main pain points and, if needed, take some time to go back to the topic that is concerning the students.

## Warmup
### Learning Objective
Engage students in active learning, giving them a challenge where they will try to solve the problem they will work on during the lesson.
### Suggested timekeeping
10 minutes
### Description
In the same way they did in the first part of the class, this time they will have a different code so they can try to style following directions. Explain that to them, recall the Agenda you’ve shown at the beginning of the class and show the challenge for students.
### Steps for conducting the class
- Check if students are in the right part of the lesson in their notebooks.
- Use the data show to share Code 02 and analyze that with students.
- Explain the challenge: They will need to try to follow the directions given in the lesson using their previous knowledge. 
- Give them 10 minutes to try to figure out how to work on the directions.
- During this 10 minutes, walk around the class, check what students are doing, answer questions when they can be quickly answered. Try to be aware of what are the main pain points of the students.
- By the end of the time, ask for some voices to show you how they would solve the problem. **Don’t give answers yet, the goal here is to make them curious and challenged.**
- Ask if someone would think of different ways to follow the instructions.
- End this part by explaining the main goal of this lesson, which is to learn some tools to help to optimize the task of styling HTML codes using CSS Combining Selectors.

## Multiple Selectors
### Learning Objective
Define the Multiple Selector, its syntaxis and proper application through the analysis and practise on a real example.
### Suggested timekeeping 
20 minutes 

### Description
In this part of the class, students will work on a different code. Given that you have Code 02 {link}, the goal of this topic is to solve the following task: **Style all the titles in blue**
### Steps to conduct the class
- Ask students how would they follow this direction.
- Explain that one option would be the addition of a separate rule for `h1`, another rule for `h2`, another for `h3` and so on until listing all the titles.
- Ask for their opinion: Would it make sense? Is there anything wrong with this solution?
- Explain that it would bring a lot of work and make the code longer and heavier, we have a better way: The multiple selections allow us to apply the same list of rules to different elements. Work in the code with the students. 
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

## Attribute selector
### Learning Objective
Define the Attribute Selector, its syntaxis and proper application through the analysis and practise on a real example.
### Suggested timekeeping 
20 minutes 
### Description 
Just like the previous topic, in this part of the lesson students will work on the Code 02. Given that you have Code 02 {link}, the goal of this topic is to solve the following task: **Style all the links with the word "hack" in their src in **green**.**

### Steps to conduct the class
- Ask to students to reflect about the question: "if we can select elements by name, why not select an element by its attributes?"
- Explain that to define an attribute for an element, you need to put them between `[]` and give them a name. 
- Ask students how they would do to solve the task. 
- Guide students on solving the task with the example Code 02. 
```css
a[href*="hack"] {
  color: green;
a {
  display: block;
}
```
- Share with the students another examples of this selector: 

| Selector             | What does it select?                  |
| -------------------- | ------------------------------------- | 
| `[attribute]`        | All elements with the specified attribute  |
| `[attribute=value]`  | All elements where the specified attribute is equal to ‘value’ |
| `[attribute~=value]` | All elements with an attribute which has a list of whitespace-separated values, one of which is exactly equal to ‘value’ |
| `[attribute|=value]` | All elements with an attribute which has a hyphen-separated list of values beginning (from the left) with "value" |
| `[attribute^=value]` | All elements with an attribute beginning with "value" |
| `[attribute$=value]` | All elements with an attribute ending with "value" |
| `[attribute*=value]` | All elements with an attribute containing the substring "value" |

## Exercise: Peer Review 

### Learning objective 
Perform a final assessment to understand the level of comprehention and application of the selectors in an independent and creative way. 

### Description
Now that students are familiar with all of the selectors, we will give them a third example of code to create their own style. They will have a time to work on the code, and after they are finished, they can submit their code to review while reviewing other's codes. 

[ // This can be a homework task, using the platform and a forum to discuss the execution of the code amongst other students. We would give them a rubric where they will have directions on how to review peer's codes. The final description and steps to this lesson depents on what would be the duration of the class and the strategy for the final evaluation.//]: # 

### Steps to conduct the class: 
- Before ending the class, go through a review of the class, summarizing what they have learned: 
- - HTML documents are represented as family trees and it is the fundamental base of the Document Object Model (DOM) 
- - Child selector is represented by the (>) signal and is used to select direct descendants to style. 
- - Descendant selector is represented by blank spaces (  ) and is used to select elements matched by the second selector, but only those which have an ancestor element matched by the first selector. 
- - Adjacent Selector is represented by the (+) signal and is used to select only the specific element that immediately follows the former specified element. 
- - We can use multiple selections to apply the same list of rules to different elements, selecting by tag names or attributes. 
- Remind students of the importance of checking the extra resources by the end of the lesson. 
- Explain students how will the final activity be performed. 
- Ask students for final considerations. 
