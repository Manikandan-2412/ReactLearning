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
 Built-in router     choose your own


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
 
   Without using the proper key  in a code then we can't able to change it and it takes more time and is iefficient

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
