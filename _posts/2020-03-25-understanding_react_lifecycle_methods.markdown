---
layout: post
title:      "Understanding React Lifecycle Methods"
date:       2020-03-25 07:34:05 -0400
permalink:  understanding_react_lifecycle_methods
---


## What are React Lifecycle Methods?

React lifecycle methods can be thought of as the series of events that happen from the very start of the development of a React component to the very end.

This involves:

   **Mounting** 
   
   *adding nodes to the DOM*
   
   **Updating**
   
   *updates to state in props*

   **Unmounting** 
   
   *removing DOM nodes*

## What the most Common Lifecycle Methods?

### Mounting

```
render()
```

*  This only method you **must** define in a React.Component subclass (all others are optional)
*  Handle![](http://)s the actual rendering of your component to the User Interface
*  Can safely read from props and state here
*  This function should be pure (returns the same result every time and does not modify the components state)

```
componentDidMount()
```

* Invoked immediately after a component is mounted 
* Used to interact with the browser
*  setState() can be called here 


### Updating

```
render()
```

* Render is also used to update within the component lifecycle
* This method is used to render the updated state and props

```
componentDidUpdate()
```

* This is invoked immediately after updating occurs
* This method is not called for the initial render.
* Commonly used when updating the DOM in response to prop or state changes.


### Unmounting

```
componentWillUnmount()
``` 
* This method is called when a component is being removed from the DOM
* Invoked immediately before a component is unmounted 
* This is the cleanup method and o nce a component is unmounted it is completely destroyed and can never be mounted again

![](https://miro.medium.com/max/2014/1*hSO--5BPT1K_YK6VqRy4vg.png)

