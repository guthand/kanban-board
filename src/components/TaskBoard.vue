<template>
    <div class="scrolling-wrapper">
        <draggable v-model="lists" class="row flex-nowrap mt-1" v-bind="getDragOptions">
            <TaskList v-for="(listItem, index) in lists" :key="index" :board="getBoard" :list="listItem"></TaskList>
        </draggable> 
    </div>
 </template>

// inserting the tasklist in the board to see the tasks we already created
//v-for and loop to get all the tasks from the lists
//getBoard to get the Board which contains the taskLists and index is the unique identity of every task
 //We can use the v-for directive to render a list of items based on an array. 
 //The v-for directive requires a special syntax in the form of item in items,
 //where items is the source data array and item is an alias for the array element being iterated on: