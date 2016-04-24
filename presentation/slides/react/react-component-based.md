## REACT SOLUTION

* HTML and JS = COUPLED and COHESIVE

```JavaScript
import React, { Component } from 'react';

export default class MyComponent extends Component{
  render ()
  {
    const { name, options, selected, answer, visible, select, post } = this.props
    return (
      <div>
          {name}
        <ul>
          {options.map(option =>
             <li key= {option}
               onClick={() => select(option)}
               style={{backgroundColor:selected===option?'yellow':''}}>
               {option}
             </li>
            )}
        </ul>
        <button onClick={() => post()}>
          {visible ? 'Restart':'Go!'}
        </button>
        {visible ? answer === selected ? 'Correct!' : 'Looser!' : ''}
      </div>);
  }
}```
