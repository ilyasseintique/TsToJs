import React from 'react'; 
we want to add type safety to props
type obj = {
  name : string;
}
const Greeting : React.FC<obj>  = ({ name }) => { 
return <div>Hello, {name}!</div>;
 };
 export default Greeting;
 
 ------------------------------------------------
 import React, { Component } from 'react';

// 1. Define the state type
type CounterState = {
  count: number;
};


class Counter extends Component<CounterProps, CounterState> {
  // 3. Initialize the typed state
  state: CounterState = {
    count: 0,
  };

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}

export default Counter;
