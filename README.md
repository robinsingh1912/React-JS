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




*. show promise chaining 
*. Promise.all vs promise.race


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
 
