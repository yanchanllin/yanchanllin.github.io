---
layout: post
title:      "Lifecycle and constructor in React"
date:       2019-08-13 19:41:25 -0400
permalink:  lifecycle_and_constructor_in_react
---

  Constructor( ) method is inside the react class component and fired before the component is mounted. It is automatically called when an object is created, it helps constructing things  to initial setup like local state and checking the arguments that were passed in. 

	  `constructor() {
        super()
           this.state = {
		// Sets that initial state
         };
	    }`
			
Also inside constructor we can bind event handlers to the component, if you aren’t binding any event handlers, you don’t need to define it in constructor. Often we can use event handler arrow function to skip the binding define part in constructor or inside when display return. 
	
    `constructor() {
        super()
           this.state = {
		// Sets that initial state
         };
	   
       // Our event handlers
        this.onClick = this.onClick.bind(this);
      // et cetera...
       }`

 After constructor( ), we call super(props) because constructor itself can not use this.props object can lead to error. Thus we take a props value from the constructor() and pass it to the super() method, it calls the constructor of the parent class. Then we can use this.props later on.

    `constructor(props) {
       super(props);
        console.log(this.props);
 
          this.state = {
          // Sets that initial state
       };

      // Our event handlers
       this.onClick = this.onClick.bind(this);
      // et cetera...
     } `
 
  Do not call setState() inside constructor( ), it can handle set the initial state of your component and constructor is the only place that you should assign the local state. Other places should rely on setState( ) this callback function performs a shallow merge of the state change into the new state. If you aren’t planning on having state in your component and aren’t binding any event handlers, you don’t need to define a constructor at all. Then you do not need a class component, use a functional component will be less code. For example:
	
  	    `const Welcome = ( ) => {
          return <h1>Hello</h1>;
         }`
		
  React lifecycle starts from initialization, mounting, updation, and unmounting. Initialization to setup props and state like inside constructor( ) method sets that initial state. Mounting starts from componentWillMount( ) to render to componentDidMount( ):
	
`class Books extends React.Component {
   constructor(props) {
      super(props);
       this.state = {
    // Sets that initial state
  };

  componentDidMount() {

  }

  componentWillUnmount() {

  }

  render() {
    return (
      <div>
        <h1>Hello</h1>
      </div>
    );
  }
 }`
 
  For example here we will not show componentWillMount( ), it is called before the render method is executed and will not see or trigger an extra rendering. componentWillMount() when invoked just before mounting occurs. It is called before render(), therefore calling setState() synchronously in this method will not get re-rendering. 
	
	`componentDidMount() {
       fetch(url).then(results => {
          // Do something with the results
            })
        }`
This is an example of using the componentDidMount method to make API calls.

 As soon as the render method hit the componentDidMount function is called, componentDidMount is better to make the request before anything is rendered. it includes the rendered component, the request is made, the state is changed, then the component is re-rendered. Next is the updation, shouldComponentUpdate will trigger to check for true or false; if returned true will hit componentWillUpdate and componentDidUpdate is called after the render method. Similar to the componentDidMount, this method can be used to perform DOM operations after the data has been updated. At last componentWillUnmount gets called before the component is removed from the DOM to clean up the task, removing any that defined in componentDidMount.
	
	`componentWillUnmount( ) {
    clearInterval(this.taskID);
     }`


