For the task magement tool it is nice to implement a drag and drop functionality as it adds much more flexibility to the app...


for the updates of the current items we will use draggable which allows us to drop items from one list to the next

We’ll use !!!  Vue-Router  !!! library to build this multi-page application using <router-view> tag to display pages

transition component — provided by Vue.js — to show smooth page transitions.

The import and export are ES6 way

Application features
This is a multi-page application with a rich feature set implemented right from the start. Below is the feature list of this app.

Boards
Allow user to,
view existing boards in the dashboard
archive and restore the boards
view individual board contents
create a new board
edit existing board information

Lists
Allow user to,
create a new list
edit list name
archive and restore lists
rearrange the lists in the board using drag and drop

List Items
Allow user to,
create new and update existing items in the list
rearrange the items in the list by drag and drop
move tasks among the lists using drag and drop

in Vue js the Html is passed through the class of the div like

header -> 
    router link is for running to the main page
    We also have to render the components for the task list and the board and add or archive !!!!

taskBoard -> 
    holds all the taks for each list-project

    draggable is the component used when we need it to be dragged to another list
    inser the taskList componet in the taskBoard so we have the task inside of every list

TaskListActions component -->  is to show Edit and Archive actions when user click on “…” in the list header.
The Edit action allows user to edit list details and archive action allows the user to archive the list

TaskListEdit
The responsibility of this component is to show a popup with the form to update list name.

TaskListRestore
The responsibility of this component is to show a popup with archived task lists. The component iterates over archivedLists array and shows task lists with a Restore button.

TaskBoardEdit
The responsibility of this component is to show a popup with the form to update the board name and description details.





template syntax  allows you to declaratively bind the rendered DOM to the underlying Vue instance's data. ... js templates are valid HTML that can be parsed by spec-compliant browsers and HTML parsers. Under the hood, Vue compiles the templates into Virtual DOM render functions.


You can use the v-model directive to create two-way data bindings on form input, textarea, and select elements. It automatically picks the correct way to update the element based on the input type. Although a bit magical, v-model is essentially syntax sugar for updating data on user input events, plus special care for some edge cases.

The directive v-if is used to conditionally render a block. The block will only be rendered if the directive’s expression returns a truthy value.

v-show will always be rendered and remain in the DOM; v-show only toggles the display CSS property of the element.

The mapGetters helper simply maps store getters to local computed properties: