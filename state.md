### Remember

Answer these on your own, then compare answers as a group

1.  What is state?
  Where you store property values to the component
  - State is where you store property values fot components
  - State is data that is managed by the component
  - State is an object in React, so we must treat it as such (this.state.name)

2.  Where do you set initial state?
  Inside the constructor and directly inside the class
  - In the component's constructor under where we call super

3.  What method do you use to update state?
  We use .setState() to update our state
  - We use the setState method
  - When we call the setState method, we need to send iin an object that specifies our targeted properties that need changed along with their new values

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

  - The code is creating a component called LeadMentor.
  - LeadMentor is displaying the questionsAnswered from its state in its return
  - The user is able to increase the amount of questionsAnswered held in state by invoking the handleClick method
  - When the state value for questionsAnswered gets updated by a button click, the component rerenders showing the updated number

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.

### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?
