
for the updates of the current items we will use draggable which allows us to drop items from one list to the next

We’ll use !!!  Vue-Router  !!! library to build this multi-page application using <router-view> tag to display pages

transition component — provided by Vue.js — to show smooth page transitions.

The import and export are ES6 way


header -> 
    router link is for running to the main page

taskBoard -> 
    holds all the taks for each list-project

    draggable is the component used when we need it to be dragged to another list
    inser the taskList componet in the taskBoard so we have the task inside of every list

The responsibility of TaskListActions component -->  is to show Edit and Archive actions when user click on “…” in the list header.
The Edit action allows user to edit list details and archive action allows the user to archive the list