### Remember

Answer these on your own, then compare answers as a group

1.  What are props?
  Props is a special word in React which stands for properties
  It is used for passing data from one component to another in a uni-directional flow
  - props is an object available to the component
  - a parent component can add key value pairs to the props object
  - props are data being passed into a component


2.  How do you pass props from a parent to a child?
  Import the parent component to the child component
  using a render method in the parent component to pass to the child
  - We pass props into the child using the child's component tag
  - We set up the props on the child's component tag by saying <whatever property name>=<hardcoded data OR a reference to existing data using curly braces>

3.  How do you access props from a class based child component?
- From within JSX, we would say {this.props.<propname>} and outside of JSX we would simply say this.props.<prop name>

4.  How do you access props from a functional component?
  - props.<prop name>

5.  How do you bind a function to a parent component so that it can be passed to a child?
  - 1) From within the constructor outside of our this.state, we would say this.<function name> = this.<function name>.bind(this)
  - 2) We can use lexical binding by not having to use the bind method AND by making our function an arrow function

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    return (
      <div className="queue-container">
        <h1>The Queue</h1>
        <h3>{this.state.questions.length}</h3>
        <h3>questions need answers</h3>
        <Student askQuestion={this.askQuestion} />
        <Mentor answerQuestion={this.answerQuestion} />
      </div>;
    )
  }
}
```
  - We are passing down separate methods to each Queue's children that, when the methods are fired from within the children, will either add a new question to Queue's this.state 

### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
