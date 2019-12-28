<template>
  <div id="app" class="container-fluid">
    <Header></Header>
    
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
