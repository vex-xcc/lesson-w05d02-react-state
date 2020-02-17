# Quiz Time for React Props and State

<br>

1. Fork and Clone this repo.
2. Put your answers in this README
3. You may use any resource except each other.
4. Submit a pull request when you're done.

<br>

**Question 1.**

A component is being passed a prop named `flavor`. What JSX would the component return in its render method to display the prop in a paragraph?

Choices:

1. `<p>My favorite ice cream is {this.props.flavor}!</p>`
2. `<p>My favorite ice cream is {props.this.flavor}!</p>`
3. `<p>My favorite ice cream is {props.flavor}!</p>`
4. `<p>My favorite ice cream is {this.flavor}!</p>`


```
1. `<p>My favorite ice cream is {this.props.flavor}!</p>`
```

<br><br>

**Question 2.** 

Is this a valid Component declaration?

```jsx
class Paintings extends Component {
  render () {
    return (
      <h1>Hello World!</h1>
      <h3>It is time for tea.</h3>
    );
  }
}
```  
  
Choices:

1. `Yes`
2. `No`


```
2. `No`
```

<br><br>

**Question 3.** 

What, specifically, happens when this method is called?

```jsx
ReactDOM.render(
  <Kangaroos />,
  document.getElementById('root')
);
```

Choices:

1. The `ReactDOM.render` method generates a virtual DOM node containing whatever content the `Kangaroos` component returns, and appends that to the element with an ID of root. Then, React compares the virtual DOM to the regular DOM and updates on the webpage only the elements that have changed.

2. The `ReactDOM.render` method generates a virtual DOM node containing whatever the JSX that the `Kangaroos` component returns. React then reloads the entire webpage, changing only the element with an ID of root.

3. The `ReactDOM.render` method returns JSX to the `Kangaroos` component, and the `Kangaroos` component returns a virtual DOM node. React updates on the webpage only the elements specified in Kangaroos that have changed.

4. The `ReactDOM.render` method generates a new element with an ID of root, which it populates with the JSX returned from the `Kangaroos` component. React updates the virtual DOM to have this new element, which the browser sees to dynamically change the page with the new element on it.


```
PUT YOUR ANSWER HERE
```


<br><br>
**Question 4.** 


If you have multiple components written in a single file, you can then have multiple default export statements at the bottom of that file - one for each component.

Choices:

1. `True`
2. `False`


```
1. `True`
```


<br><br>
**Question 5.** 



How could you use `create-react-app` to create a new app called jungle_maze?

Choices:

1. `create-react-app npm/start jungle_maze`
2. `create-react-app jungle_maze.js`
3. `create-react-app jungle_maze`
4. `create-react-app index/jungle_maze.js`


```
3. `create-react-app jungle_maze`
```

<br><br>

**Question 6.** 

Take a look at the following React file. Choose the reason(s) it won't run properly.

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import Store from './Store.js';

const groceryList = {
  important: "milk",
  spices: [
    "pepper",
    "salt"
  ]
}

ReactDOM.render(
  <Store
    buy_me={groceryList.milk}
    me_too={groceryList.spices}
  >,
  document.getElementById('root')
);
```

Choices:

1. The Store component call needs to end with `/>`, not just `>`
2. The prop name and variable name need to match - `buy_me` needs to be `milk` and `me_too` needs to be `spices`
3. The `var groceryList` declaration needs to be inside the render method
4. When passing the props into `Store`, the syntax is `this.groceryList.important` and `this.groceryList.spices`
5. The `buy_me={groceryList.milk}` prop should be `buy_me={groceryList.important}`


```
1. The Store component call needs to end with `/>`, not just `>`
5. The `buy_me={groceryList.milk}` prop should be `buy_me={groceryList.important}`
```

<br><br>

**Question 7.** 

If I'm displaying multiple nested components, assuming the `Flowers` component is being passed all necessary props and the `Daisy` component is imported and written correctly, is this valid syntax?

```jsx
import React, { Component } from 'react';
import Daisy from './Daisy.js';

class Flowers extends Component {
  render() {
    const allDaisies = [
      <Daisy body={this.props.spring} />,
      <Daisy body={this.props.rabbits} />
    ];

    return (
      <div>
        <h1>{this.props.favorites}</h1>
        <h3>Daisies:</h3>
        {allDaisies}
      </div>
    );
  }
}
```

Choices:

1. `Yes`
2. `No`


```
1. `Yes`
```


<br><br>

**Question 8.** 

Where does `constructor()` go, and when do you need it?


Choices:

1. At the top of the component class; you always need it for accurate setup of that class.

2. At the top of the component class; you only need it if you are changing any initial configurations for that class.

3. In the component class' `render()` method; you always need it for accurate setup of that class.

4. In the component class' `render()` method;  you only need it if you are changing any initial configurations for that class.


```
2. At the top of the component class; you only need it if you are changing any initial configurations for that class.
```


<br><br>

**Question 9.** 


What happens when you call `setState()`?

Choices:

1. The new state will be passed into the current state of the component. The virtual DOM tree is updated. A diff is run between the virtual DOM tree and the regular DOM tree. Only the correspondingly elements in the regular DOM tree will update.

2. The virtual DOM tree is updated. A diff is run between the virtual DOM tree and the regular DOM tree. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.

3. The virtual DOM tree is updated. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.


4. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.


```

1. The new state will be passed into the current state of the component. The virtual DOM tree is updated. A diff is run between the virtual DOM tree and the regular DOM tree. Only the correspondingly elements in the regular DOM tree will update.```

<br><br>

**Question 10.** 

If we have the code below, inside of the Painting component, will `dinosaur` be treated as a prop or a state?

```html
<Painting dinosaur="velociraptor" />
```

Choices:

1. `prop`
2. `state`


```
1. `prop`
```

<br><br>

**Question 11.** 


What is wrong with the below code? Choose all that apply.

```jsx
class Compliment extends Component {
  constructor () {
    state = {
      compliment = "You're so awesome!"
    };
  }
}
```

Choices:

1. You can't have a state with the same name as the component

2. State is set with `this.state`, not just `state`

3. State is set with colons, not equal signs. It should be `compliment: "You're so awesome!"`

4. Constructors need to begin with a call to `super()`

5. All of the above.


```
5. All of the above.
```


<br><br>

**Question 12.** 


Using React, if you refresh a webpage, you never lose information since everything is stored in the component or browser state.

Choices:

1. `True`
2. `False`


```
1. `True`
```


<br><br>

**Question 13.** 

What is `map`?

Choices:

1. A map is like a `while` loop. With `map`, you use an existing iterator to navigate through each item until you break the loop.

2. A map is like a `for` loop. With `map`, you use an existing iterator to navigate through each item in an array.

3. A map is like a `for` loop. With `map`, you make a new variable and with it iterate through each item in an array.

4. A map is like a `while` loop. With `map`, you make a new variable and with it iterate through each item until you break the loop.


```
3. A map is like a `for` loop. With `map`, you make a new variable and with it iterate through each item in an array.
```


<br><br>

**Question 14.** 

Is the correct syntax for `map`?

```js
const drinks = ['tea', 'espresso', 'milkshake'];

const myDrinks = drinks.map( (soda, index) => {
  return 'I love' + soda;
});
```

Choices:

1. No - `soda` was never initialized
2. No - `index` is a keyword and cannot be used as a variable
3. No - the first line of the function should be `const myDrinks = map( (drinks, index)`
4. Yes


```
4. Yes
```



<br><br>

**Question 15.** 

Is the correct syntax for `map`, if the array is a prop named `Juice`?

```jsx
const Juices = this.prop.Juice.map((juiceType, index) => {
  return cuteJuice = 'I love' + juiceType;
});
```

Choices:

1. No - the array should be called with `this.props.Juice`, making it `this.props.Juice.map`

2. No - the array should be called with `Juice`, making it simply `Juice.map`

3. No - `juiceType` was never initialized

4. Yes


```
2. No - the array should be called with `Juice`, making it simply `Juice.map`
```


<br>
