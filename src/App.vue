<template>
  <div id="app" class="container-fluid">
    <Header></Header>
      <transition name="page" mode="out-in" v-if="!isLoading">
        <router-view></router-view>
      </transition>
      <ComponentIsLoading></ComponentIsLoading>
  </div>
</template>

<script>
import KanbanBoard from './components/KanbanBoard.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
      KanbanBoard,
      Header
  }
}
</script>

<style lang="scss">
  @import './assets/app.scss';
</style>


// Vue provides a transition wrapper component, allowing you to add entering/leaving transitions for any element or component in the following contexts:
// router-view wrapped with transition is for smoother routing throughout the pages