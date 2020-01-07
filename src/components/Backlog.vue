<template>
  <div class="backlog-view">
    <new-item />

    <div
      v-for="item in items"
      :key="item.id"
      class="card"
    >
      <div class="card-block">
        <h5 class="card-title">
          <span class="text"> #{{ item.id }}</span>
          {{ item.text }}
          <span :class="badgeClass(item)">{{ badgeText(item) }}</span>
        </h5>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
import NewItemForm from './NewItemForm';
const badgeDetail = {
  todo: {
    text: 'todo',
    class: 'badge badge-light'
  },
  inProgress: {
    text: 'in progress',
    class: 'badge badge-info'
  },
  done: {
    text: 'done',
    class: 'badge badge-success'
  }
};
export default {
  name: 'Backlog',
  components: {
    'new-item': NewItemForm
  },
  computed: mapState({
    items: s => [...s.items.todo, ...s.items.inProgress, ...s.items.done]
  }),
  methods: {
    itemLane(item) {
      if (this.$store.state.items.todo.includes(item)) {
        return 'todo';
      }
      if (this.$store.state.items.inProgress.includes(item)) {
        return 'inProgress';
      }
      return 'done';
    },
    badgeText(item) {
      const lane = this.itemLane(item);
      return badgeDetail[lane].text;
    },
    badgeClass(item) {
      const lane = this.itemLane(item);
      return badgeDetail[lane].class;
    }
  }
};
</script>

// v for items maps through the items
// the items have their own id by numbers and we give their name
//So how do we display state inside the store in our Vue components? 
//Since Vuex stores are reactive, the simplest way to "retrieve" state from it is 
//simply returning some store state from within a computed property(see above)
//Whenever store.state.count changes, it will cause the computed property to re-evaluate, (as the DOM)
 and trigger associated DOM updates.

 on line 42 on there are the methods on how to render the items which ew add
 //itemlane is the status of the item