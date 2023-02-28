---
date: '2023-02-28T19:04:23.598Z'
title: React Component Life Cycle with Functional Components
tagline: React Component Life Cycle with Functional Components
preview: >-
  React components have a life cycle, which consists of various phases from
  initialization to rendering to updating and unmounting. Understanding the
  component life cycle is crucial for building efficient and optimized React
  applications. In this post, we will explore the component life cycle with
  functional components.
image: 'https://storage.googleapis.com/portfolio-imagens/functional-components.png'
category: React
---
React is a popular JavaScript library used for building user interfaces. In React, function components are a simpler and more concise way to create components than class components. In this post, we'll discuss the life cycle of function components in React.

# The Basic Life Cycle
Function components have a basic life cycle consisting of two phases:

* **Mounting**: This phase occurs when the component is first created and added to the DOM.

* **Updating**: This phase occurs when the component's state or props change.

# Mounting Phase
The mounting phase of a function component has the following life cycle methods:

* **useState()** - This is a hook that initializes and updates state in a functional component.

* **useEffect()** - This hook is used to perform side effects, such as fetching data or updating the DOM, after the component has mounted.

Here's an example of how to use these hooks in a simple function component:

```jsx
import React, { useState, useEffect } from 'react';

function MyComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

```


In this example, the useState() hook is used to initialize the state variable count to 0, and the useEffect() hook is used to update the document title after every state update.

# Updating Phase
The updating phase of a function component has the following life cycle methods:

* **useState()** - This hook is used to update state in a functional component.

* **useEffect()** - This hook is used to perform side effects after the component has updated.

Here's an example of how to use these hooks in a function component that updates its state based on a prop:

```jsx
import React, { useState, useEffect } from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(props.initialCount);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

export default function App() {
  return <MyComponent initialCount={0} />;
}

```


In this example, the useState() hook is used to update the state variable count whenever the prop initialCount changes.


# Advanced Life Cycle
In addition to the basic life cycle, function components also have a few advanced life cycle methods:

* **useContext()** - This hook is used to access data from a parent component's context.

* **useReducer()** - This hook is used to manage more complex state logic in a functional component.

* **useCallback()** - This hook is used to memoize functions to prevent unnecessary re-renders.

* **useMemo()** - This hook is used to memoize values to prevent unnecessary re-renders.

* **useRef()** - This hook is used to create mutable variables that persist across renders.

# Conclusion
In conclusion, function components provide a simpler and more concise way to create components in React. Understanding the life cycle of function components is essential for building robust and efficient applications. By using hooks like useState(), useEffect(), useContext(), useReducer(), useCallback(), useMemo(), and useRef(), developers can take advantage of the advanced features available in React functional components.

As with any skill, it takes time and practice to become proficient in React. However, with the resources available online, including documentation, tutorials, and communities, anyone can learn to build powerful applications with React functional components.

