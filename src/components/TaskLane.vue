<template>
  <div class="card">
    <h3 class="card-header">
      {{ title }}
    </h3>
    <div class="card-body">
      <draggable
        v-model="draggables"
        :options="{ group: 'default' }"
      >
        <div
          v-for="item in items"
          :key="item.id"
        >
          <item :item="item" />
        </div>
      </draggable>
    </div>
    <div class="card-footer text">
      {{ itemCount }}
    </div>
  </div>
</template>

<script>
import Draggable from 'vuedraggable';
import TaskLaneItem from './TaskLaneItem';
export default {
  name: 'TaskLane',
  components: {
    item: TaskLaneItem,
    draggable: Draggable
  },
  props: {items: { type:String , default: 'items'},title: { type:String , default: 'title'}
  ,id: { type:String , default: 'id'} },
  
  computed: {
    itemCount() {
      if (!this.items) return '';
      if (this.items.length === 1) return '1 task';
      return `${this.items.length} tasks`;
    },
    draggables: {
      get() {
        return this.items;
      },
      set(items) {
        this.$store.commit('updateItems', {
          items,
          id: this.id
        });
      }
    }
  }
};
</script>

<style>
.card-body > * {
  min-height: 50px;
}
</style>

//taskLane of the item is the status and its position
//imported the draggable element so we can move items from one list to the other
//counting the items with the conditional statement
// we also use the setter and getter to update the items