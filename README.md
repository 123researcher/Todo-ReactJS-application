# Todo-ReactJS-application

The first step is to create a new React app. From your command line, navigate to the folder you want to create your new project, and enter the following:

create-react-app todolist
Press Enter/Return to run that command. A few moments later, a brand new React project will get created. Since we want to start from a blank slate, we are going to delete everything contained in our public folder and in our src folder.

By now, you know the drill. We need a starting point, so go ahead and create a new HTML document inside our public folder called index.html. Inside it, add the following content:


## Creating the Initial UI
 The first thing we are going to do to is get our input field and button to appear. This is all done by using the div, form, input, and button elements!

All of that will live inside a component we are going to call TodoList. In your src folder, add a file called TodoList.js. Inside this file, add the following things:



There is a bunch of JSX that gets our form elements up and running. To use our newly created TodoList component, let's go back to index.js and reference it to see what our app looks like right now. Go ahead and make the following two changes:

Building the Rest of the App
As you can imagine, getting the initial UI elements to show up is the easy part. Tying up all of the various visuals with the underlying data is where the real work lies. This work can roughly be divided into five parts:

Adding items
Displaying items
Styling
Removing items
Animating items as they are added or removed
Individually, all of these little implementation details are easy to wrap our brain around. When we put them together, there are a few things to watch out for. We will look at all that and more in the following sections.

Adding Items
The first major thing we'll tackle is setting up the event handlers and default form handling behavior to allow us to add an item. Go back to our form element and make the following highlighted change:


We listen for the submit event on the form itself, and we call the addItem method when that event is overheard. Notice that we aren't listening for any event on the button itself. The reason is that our button has a type attribute set to submit. This is one of those HTML trickeries where clicking on the button whose type is submit is the equivalent of the submit event on the form being fired.
