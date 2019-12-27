<template>
  <div class="col-3 list-column list-width">
    <div class="heading" style="{ backgroundColor: list.headerColor }">
      <h3 class="heading-text text-center"> {{ list.name }} </h3>
      <TaskListActions :board="board" :lists="list"></TaskListActions>
      </div>
      <div class="cards cards-list">
        <draggable v-model="items" v-bind="dragOptions">
          <TaskListItem 
          v-for="item in items"
          :item="item"
          :list="list"
          :board="board"
          :key="item.id"
          ></TaskListItem>
        </draggable>
  </div>
</template>

<script>
export default {
  name: 'KanbanBoard'
}
</script>