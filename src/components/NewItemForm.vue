<template>
    <div class="add-item">
        <form action="#" method="post" v-on:submit.prevent="submitForm">
            <input type="text" v-model="itemText" placeholder="Add something to the backlog">
        </form>
    </div>
</template>

<script>
export default {
  name: 'NewItemForm',
  data() {
    return {
      itemText: ''
    };
  },
  methods: {
    submitForm() {
      if (this.itemText) {
        this.$store.commit('addItem', {
          text: this.itemText
        });
        this.itemText = '';
      }
    }
  }
};
</script>

<style>
.add-item input {
  outline: none;
  border: 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.5);
  width: 100%;
  transition: all 0.25s;
  background: inherit;
  color: rgb(68, 31, 31);
}
.add-item input:focus {
  border-bottom-color: rgba(255, 255, 255, 1);
}
.add-item {
  margin: 30px 0;
}
</style>

// form to create new tasks
// uses the post method to add the task to the form
//submits to the backlog and to the todo list
//a component’s data option must be a function, 
//so that each instance can maintain an independent copy of the returned data object:
