<template>
  <div class="board">
    <div class="row">
      <div class="col-md">
        <task-lane
          id="todo"
          title="Todo"
          :items="todoItems"
        />
      </div>
      <div class="col-md">
        <task-lane
          id="inProgress"
          title="In progress"
          :items="inProgressItems"
        />
      </div>
      <div class="col-md">
        <task-lane
          id="done"
          title="Done"
          :items="doneItems"
        />
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
import TaskLane from './TaskLane';
export default {
  name: 'KanbanBoard',
  components: {
    'task-lane': TaskLane
  },
  computed: mapState({
    todoItems: s => s.items.todo,
    inProgressItems: s => s.items.inProgress,
    doneItems: s => s.items.done
  })
};
</script>

// kanban board contains the all the tasks we added divided in columns 
// we also import and export standard things
// we also use mapState to return the items of the list in the KanbanBoard as we refer in the backlog