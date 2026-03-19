# ReactLearning
ReactLearn
React:

    JavaScript library for building UIs
    Created by Facebook(Meta) 2013
    Component-based architecture
    Power Netflix, Airbnb , Instagram


React is not a framework

 Framework           Library
 
 Full solution      Focused solution
 Angular, Vue       React
 More opionionated  More flexible
 Built-in router    choose your own


JSX --> JavaScript Meets HTML
 
writing a html element in a javascript is known as JSX

is used to complie like this -->
const element = React.createElement('h1',null,'Hello, React!');

JSX Rules
 1.Single parent element
 2.className instead of class
 3.All tags must be closed
 4.Javascript in {curly braces}
 5.Inline Styles use camelCase


Fragment is simply used like an <div> in react
Syntax:
   <>
   // code of all
 
   </>

React application is always used by the vite
---
ClassName & HTMLFOR:

The class is not there in a react only there is attribute we need to use the classname for that
for is also not there in a react only there is attribute we need to use htmlFor for that
---
Closing all the Tags:

 It is a mandantory thing we need to close the tags

<input img="something.png" />--> this is how the tags are used to close
---
JavaScript expression we can't able to use in react

the default value for the input is given as the value attribute
In JSX --> the value is used to make the default value
       --> the defaultvalue is used to make the value can be editable

---
Inline Styles
     All the properties for use in JSX we need to use Objects for all the inline properties

   const styles ={
                backgroundColor : 'red',
                color: 'white'
 }
 

<p style={styles}> The normal text </p>
  the "" is not used here, here only the {} brackets for the assigning a value.
this is how all the elements are use in the area.

---
Virtual DOM  (React's SuperPower)

Rendering is a process of showing something in a webpage by some or more code in a platform

The actual problem in JavaScript DOM is really slow

Working with a javascript and the browser is a single threaded. everything is working in a same thread and when the heavy loaded the thread gets locked and the ui is not showing in proper way so this is a major problem.

Due to the single thread only the page of the browser is often getting refresh.

---->  the is problem in a actual code which is running and we need to change the particular UI
       Virtual DOM -->  create a new virtual copy of  previous DOM  and the make the difference of the requirement and the previous dom,
                        (diff phase)
 
                        After all the process the change has been made in a Real DOM --> This is known as Virtual DOM (This is how the virtual dom is works).


 
 React creates a Light Weight copy
 Compares the old Dom Vs New (Diff)
 Calculates Minimum changes
 Only  update what has been changed

  Reconciliation process:

          State change
             |
         New Virtual DOM Created
             |
         Diff With previous DOM
             |
         Calculate the Minimum updates
             |
         Batch Update real DOM

Why keys is really matter :
 
   Without using the proper key  in a code then we can't able to change it and it takes more time and is inefficient

Always use the key which makes the unique and efficient

---
Components (Building Blocks of react)

Creating a function and return the html element

function Welcome ({name}) { return <h1> Hello,{name} !</h1>; }
                     |
                     Props
Class Components(legacy)

class welcome extends React.Component {
 render(){
   return <h1> Hello,{this.props.name}!</h1>;
}

}
---
Props - Component Communication

request different values from outside

simply the props is a like a parameter


The children props:
------------------
while using the child props in the ts file just use the React.PropsWithChildren to encounter the error

in simple --> using children props we can able to pass different component as props(parameters) for rending

(card is simply used in the example and using className for the further )

----------------------------------------------------------------------------

Event Handlers :
Making components interactive
---------------------

basic eventhandlers in the react:
-------------------------------

function Button(){
     const handleClick = ()=>{
     alert('button is clicked');
     };

     return <button onClick = {handleClick} > click me</button>
}

Common Events for event handling:
------------

In React, event handling works similarly to DOM events but uses camelCase naming and passes a synthetic event object for cross-browser compatibility.
Here’s a list of common events grouped by category:

1. Mouse Events

onClick – Triggered when an element is clicked.
onDoubleClick – Triggered on double-click.
onMouseEnter – Fires when the mouse enters an element.
onMouseLeave – Fires when the mouse leaves an element.
onMouseMove – Fires when the mouse moves over an element.
onMouseDown – Fires when a mouse button is pressed.
onMouseUp – Fires when a mouse button is released.


2. Keyboard Events

onKeyDown – Fires when a key is pressed.
onKeyUp – Fires when a key is released.
onKeyPress (deprecated in modern browsers) – Use onKeyDown or onKeyUp instead.


3. Form Events

onChange – Fires when the value of an input, textarea, or select changes.
onInput – Fires when the user types or changes input value.
onSubmit – Fires when a form is submitted.
onFocus – Fires when an element gains focus.
onBlur – Fires when an element loses focus.


4. Clipboard Events

onCopy – Fires when content is copied.
onCut – Fires when content is cut.
onPaste – Fires when content is pasted.


5. Focus Events

onFocus – Element gains focus.
onBlur – Element loses focus.


6. Touch Events (for mobile/touch devices)

onTouchStart – Fires when a touch starts.
onTouchMove – Fires when a touch moves.
onTouchEnd – Fires when a touch ends.
onTouchCancel – Fires when a touch is interrupted.


Example Usage
Jsximport React from "react";

function EventExample() {
  const handleClick = () => {
    alert("Button clicked!");
  };

  const handleChange = (e) => {
    console.log("Input value:", e.target.value);
  };

  return (
    <div>
      <button onClick={handleClick}>Click Me</button>
      <input type="text" onChange={handleChange} placeholder="Type something" />
    </div>
  );
}

export default EventExample;

===========================================================================
Event parameters:
----------------
the event parameter is usually used to identify which function or which is actually called
function eventparameter(){
     const handleClick = (event)=>{
     Console.log(event.target) // the clicked element
     event.preDefault()
     event.stopProgation()
     };

     return <button onClick = {handleClick} > click me</button>
}

==============================================================================
Conditional Rendering
showing/hiding content dynamically:
----------------------------------
is actually tell about the existing on the dom or not exist on the dom 
is a type of rendering something or not rendering something in a dynamic way.

Ternary Operator:
----------------
Normal but using a jsx we can able to do it in the react

function something (){
return (<div>
{
   isLoggedIn ?
   (<h1>Welcome to learning</h1>):
   (<h1>you need to learn something<h1>)
}
</div>);
}
this is the normal operation

Logical And:
-----------
&& is used.

================================================================================

Looping & List 
Rendering dynamic data:
-----------------------
All of the things are using the Key for mapping and faster duration
Array Mapping
filtering a different list

State Management:
Making component dynamic
----------------
Use state Hook
Usestate Anatonmy  --> usestate for assigning something 
    
