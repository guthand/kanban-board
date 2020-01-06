// store file contains the lists with the items
// backlog contains the new item action and the backlog items
// the kanbanboard contains all the tasks no matter where they are and you can move them from onw class to the other
the menu bar could be our header
// the new item form contains the method to create new tasks
//the task lane contains the number of the items and the draggable action
// the task lane item is imported in the taskLane
// index in router contains the routing in the web app

// 


Backlog

// v for items maps through the items
// the items have their own id by numbers and we give their name
//So how do we display state inside the store in our Vue components? 
//Since Vuex stores are reactive, the simplest way to "retrieve" state from it is 
//simply returning some store state from within a computed property(see above)
//Whenever store.state.count changes, it will cause the computed property to re-evaluate, (as the DOM)
 and trigger associated DOM updates.

 on line 42 on there are the methods on how to render the items which ew add
  //itemlane is the status of the item

KanbanBoard

// kanban board contains the all the tasks we added divided in columns 
// we also import and export standard things
// we also use mapState to return the items of the list in the KanbanBoard as we refer in the backlog


MenuBar

// The menu bar is the header of the app 
// contains the routes to the board and the backlog page to add tasks
// Buttons for navigation and text display

NewItemsForm

// form to create new tasks
// uses the post method to add the task to the form
//submits to the backlog and to the todo list
//a component’s data option must be a function, 
//so that each instance can maintain an independent copy of the returned data object:


  //TaskLane

//taskLane of the item is the status and its position
//imported the draggable element so we can move items from one list to the other
//counting the items with the conditional statement
// we also use the setter and getter to update the items

TaskLaneItem

// definition of the laneItem
// it is the component that can go from lane to lane
// item passed as props to the list
// its id is going according to the time of creation