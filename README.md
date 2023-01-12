# React-JS
## theory
1. React vs Angular
- ui libray | complete framework
- one way data binding | two way data binding 
- SPA | SPA

2. Differnent ways you make make an api call??
- Fetch API
- Axios

3. React flow and why its called SPA with one way data binding??
- A single-page application (SPA) is a webpage that dynamically interacts with the web browser by rewriting the current web page with data from the webserver. As a result, the webpage does not reload during its execution and instead operates in a browser. update the one single html page .

4. how can you pass data from child to parent? write an example.
- with callback we can pass eventhandler to update the state of parent component.
```
import {useState} from 'react';

function Child({handleClick}) {
  return (
    <div>
      <button onClick={event => handleClick(100)}>Click</button>
    </div>
  );
}

export default function Parent() {
  const [count, setCount] = useState(0);

  const handleClick = num => {
    // 👇️ take parameter passed from Child component
    setCount(current => current + num);
  };

  return (
    <div>
      <Child handleClick={handleClick} />

      <h2>Count: {count}</h2>
    </div>
  );
}

```
5. functional vs class components
- functional components are plain javascript function | class components require to extend React.Component
- no render method | It has render method which bassicaly return JSX
- represend ui and use hooks | react lifecycle methods and state can we used
- no need to contructor | need to constructor 
- no need to bind this | need to bind eventhandlers

6. Shadow DOM vs Virtual DO
- An API to attach hidden DOM to an element for encapculation purpose | An in-memory representation of Actual DOM
- In short, the shadow DOM is a browser technology whose main objective is to provide encapsulation when creating elements. On the other hand, the virtual DOM is managed by JavaScript libraries—e.g., React—and it’s mostly a strategy to optimize performance.

7. VDOM ?? How it works ?? Diffing Algorithim, Reconciliation ??
- https://reactjs.org/docs/reconciliation.html 

8. what is context API? can we have multiple provider ? example ?
- Context is a built-in API introduced in React. It makes it possible to pass data from parent to children nested deep down the component tree directly, instead of passing it down through a chain of props. 
- Yes we can have multiple provider



*. show promise chaining 

*. Promise.all vs promise.race

*. Desgin patterns
- HOC pattern
- Render props pattern
- Hooks pattern
- Compound pattern





 ## coding 
find twoPairSum  = k
___
example 
[1,2,4,5,6,7] , k = 5
[1,4]


snake_case to camelCase and vice versa

remove duplicated

find dupplicate and missing number sum 
___

[1,2,4,4,5,6] missing is 3 and duplicate is 4


 Create Balanced Parentheses
 ___
 
 Write a function to add parentheses so that all opening and closing parentheses have matching counterparts. 
 You will do this by appending parentheses to the beginning or end of the string. 
 The result should contain the original string and be of minimal length.
  
 The input will be a string of varying length, only containing '(' and/or ')'.
 Ex:
 "))" outputs >> "(())"
 ")(" outputs >> "()()"
 "))))(()(" outputs >> "(((())))(()())"
 
