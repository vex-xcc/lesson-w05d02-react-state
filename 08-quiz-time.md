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

**Answer**

Correct answer: 1
>Explanation: You distinguish JavaScript in JSX with curly braces {}. The syntax to refer to the prop is this.props.flavor - which says, "in this file, find a prop, named 'flavor'".


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

**Answer**

No
>Explanation: No, because the render method can only return one JSX element. To make this valid, the two heading tags need to be wrapped in a single tag. For example, the render method could return a `<div>` with the `<h1>` and `<h3>` elements inside of it

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

**Answer**

Correct Answer: 1


<br><br>
**Question 4.** 


If you have multiple components written in a single file, you can then have multiple default export statements at the bottom of that file - one for each component.

Choices:

1. `True`
2. `False`

**Answer**

False 
>Explanation: Only one default is allowed per file. The default keyword means that if we try to import anything from this file that the app can't find, JavaScript will automatically revert to importing the component exported as default instead. If there are multiple default statements, the app won't know what to do! On a side note, it is best practice to split different components into their own file, so hopefully you won't run into this issue.


<br><br>
**Question 5.** 



How could you use `create-react-app` to create a new app called jungle_maze?

Choices:

1. `create-react-app npm/start jungle_maze`
2. `create-react-app jungle_maze.js`
3. `create-react-app jungle_maze`
4. `create-react-app index/jungle_maze.js`

**Answer**

Correct Answer: 3
>Explanation: It's simple to create an app using create-react-app - just call the tool with the name you want for your app. In this case, create-react-app jungle_maze

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

**Answer**

Correct Answer: 1, 5
>Explanation: The component needs to end with /> to close the tag. Without adding the props, it would look like `<Store />`
>Also, when you're calling an item within an object you should call it by its key not value, so `groceryList.important`

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
    ]

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

**Answer**

Yes
>Explanation: It is! You can pass JavaScript objects into JSX using {} curly braces. Just as we can add to the JSX the passed in props, we can also add to the JSX the variable allDaisies by putting {allDaisies}


<br><br>

**Question 8.** 

Where does `constructor()` go, and when do you need it?


Choices:

1. At the top of the component class; you always need it for accurate setup of that class.

2. At the top of the component class; you only need it if you are changing any initial configurations for that class.

3. In the component class' `render()` method; you always need it for accurate setup of that class.

4. In the component class' `render()` method;  you only need it if you are changing any initial configurations for that class.

**Answer**

Correct Answer: 2
>Explanation: The constructor is only needed if you're changing initial setup - like setting a state. It is its own method and goes at the top of the component class, not inside the render method.


<br><br>

**Question 9.** 


What happens when you call `setState()`?

Choices:

1. The new state will be passed into the current state of the component. The virtual DOM tree is updated. A diff is run between the virtual DOM tree and the regular DOM tree. Only the correspondingly elements in the regular DOM tree will update.

2. The virtual DOM tree is updated. A diff is run between the virtual DOM tree and the regular DOM tree. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.

3. The virtual DOM tree is updated. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.


4. The new state will be passed into the current state of the component. Only the correspondingly elements in the regular DOM tree will update.

**Answer**

Correct answer: 1
>Explanation: setState() first updates the state of the component; this causes the virtual DOM to be updated, which in turn triggers React to compare the virtual DOM and regular DOM. Only the changed elements will update.

<br><br>

**Question 10.** 

If we have the code below, inside of the Painting component, will `dinosaur` be treated as a prop or a state?

```html
<Painting dinosaur="velociraptor" />
```

Choices:

1. `prop`
2. `state`

**Answer**

props
>Explanation: Elements that are passed in to a component are treated as a prop within that component. For dinosaur to be considered a state within Painting, it would need to be a new element declared within Painting's constructor - not passed in to Painting.

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

**Answer**

2, 3, and 4 are correct


<br><br>

**Question 12.** 


Using React, if you refresh a webpage, you never lose information since everything is stored in the component or browser state.

Choices:

1. `True`
2. `False`

**Answer**

False


<br><br>

**Question 13.** 

What is `map`?

Choices:

1. A map is like a `while` loop. With `map`, you use an existing iterator to navigate through each item until you break the loop.

2. A map is like a `for` loop. With `map`, you use an existing iterator to navigate through each item in an array.

3. A map is like a `for` loop. With `map`, you make a new variable and with it iterate through each item in an array.

4. A map is like a `while` loop. With `map`, you make a new variable and with it iterate through each item until you break the loop.

**Answer**

Correct answer: 3
>Explanation: Right! We use map to iterate over an array, like a for loop, and perform an action on each item, usually saving this into a new variable.


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

**Answer**

Yes



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

**Answer**

Correct Answer: 1
>Explanation: It's not, because while all of the map specific syntax is correct, you would call the prop with this.props.Juice - with an `s` on props.


<br>
