<template>
    <div class="scrolling-wrapper">
        <draggable v-model="lists" class="row flex-nowrap mt-1" v-bind="getDragOptions">
            <TaskList v-for="(listItem, index) in lists" :key="index" :board="getBoard" :list="listItem"></TaskList>
        </draggable> 
    </div>
 </template>

 //We can use the v-for directive to render a list of items based on an array. 
 //The v-for directive requires a special syntax in the form of item in items,
 //where items is the source data array and item is an alias for the array element being iterated on: