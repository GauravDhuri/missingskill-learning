# <span class="header">Flutter</span>

<span class="highlight">Flutter is Google's UI toolkit for building beautiful, natively compiled applications for mobile, web, desktop, and embedded devices from a single codebase</span> .

Some advantages of using Flutter are :-
* Modern and reactive framework
* Uses dart which is easy to learn
* Fast development
* Same UI can run over multiple application
* Fluid and aesthetic interfaces

# <span class="header">Widgets</span>

<span class="highlight">Just like how Almost everything is JS is an object, In flutter everything is widget</span> . In fact the application itself can be considered as Widget. Widget are basically user interface components used to create interface.

Most Important widgets used in creating any app :-
* <span class="list">MyApp</span> - User created Widget/Root of the application
* <span class="list">MaterialApp</span> - home property to specify user interface
* <span class="list">Scaffold></span> - has two properties - body and appbar

## <span class="header2">Types of Widget</span>

There are two types of Widget in flutter :-
* Stateless Widget
* Stateful Widget

Understanding these widget type is very important as it also helps us understand how flutter does the sate-management of the application.

### <span class="header3">Stateless Widgets</span>

<span class="highlight">Stateless widgets are widgets that do not change or will not change in the future</span> . They only run once when the app is created. Basically, something like a Text field that will not change over time.

### <span class="header3">Stateful Widgets</span>

<span class="highlight">Stateful widgets are widget that can change over time</span> . It is a dynamic in nature. These widget hold the state i.e information. When the state of the widget changes the UI is rebuilt again, something like checkbox which can have two states, checked and unchecked.

# <span class="header">Flutter Layout</span>

Not going into too much detail. flutter layout widgets can be grouped into two types based on its child :-
* Widget with single child
* Widget with multiple child

## <span class="header2">Single Child</span>

Single child Widget can be often deceiving. At first encounter, we often think of them as a widget that hold only one entity, which is true. However, we can form chain of single child to make use of multiple single child Widget.


<img src="../assests/Wigetsingle.jpg" width="500">


Single child Widget includes :-
* Container
* Text
* Center
* Padding
* Align

## <span class="header2">Multi Child</span>

As the name suggest multi-child widgets can hold multiple widgets into them. We often refer to it as children.


<img src="../assests/Widgetmultiple.jpg" width="500" height="600">


Multi-Child Widgets include :-
* Row
* Column
* Expanded
* ListView
* Stack

# <span class="header">Other Features</span>

Not dragging this too much, Flutter provides developers with many other features that help us create precise and fluid UI.

Some of features are :-
* Gestures
* Animations
* Accessing Rest API
* Quick Navigation & Routing
* Splash Screens
* Drawers
* Toasts
* Snackbar
* Progress bar

Also, Along with these features, we can also add third party packages that can come with their own distinct features.


<br>
<br>
<br>
<style>
.highlight{
  color: #75FF33
}
.header3{
  color: #E6D100
}
.header{
  color: #EE82EE
}
.header2{
  color: #00FFFF
}
.list{
  color: #FF8080
}
</style>