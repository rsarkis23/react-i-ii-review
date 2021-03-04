### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
React is an open-source, front end, JavaScript library. it is maintained by Facebook and a community of individual developers and companies
  - Is a JS based library run by Facebook
  - Used to manage the DOM and create highly performant user interfaces
  - Uses component based architecture and unidirectional data flow
  - Has it's own virtual DOM

2.  What is create-react-app?
Create React App is a tool that helps start the process of building React apps.  It sets up your project after running the Create React App command
  - A package that sets up a new React project
  - Also sets up a developer server that will auto-refresh on changes

3.  What is Component Based Architecture?
Component-based architecture is the decomposition 
  - the concept of encapsulating individual pieces of code to bring together into a larger project/app

4.  What is JSX?
is the use of JavaScript with html
  - It is the syntax that React uses (looks very much like HTML)
  - It is eventually transpiled into regular JS function calls
  - JSX is not special only to React

5.  What is the virtual DOM?
  - A lightweight copy of the actual DOM
  - React updates the virtual DOM when any changes to a component are made, then uses the virtual DOM to decide what parts of the actual DOM to change, only updates that need to be updated

6.  What is unidirectional (one-way) data flow?
  - Data can only flow one way to other parts of the application (e,g,, parent to child using props)
  - This ensures we a have a "Single Source of Truth"

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
  -

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
