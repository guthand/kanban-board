<template>
    <div class="scrolling-wrapper">
        <draggable v-model="lists" class="row flex-nowrap mt-1" v-bind="getDragOptions">
            <TaskList v-for="(listItem, index) in lists" :key="index" :board="getBoard" :list="listItem"></TaskList>
        </draggable> 
    </div>
 </template>