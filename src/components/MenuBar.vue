<template>
  <div class="menubar">
    <div
      class="btn-group"
      role="group"
      aria-label="Menu bar"
    >
      <router-link
        to="/board"
        :class="buttonClass('/board')"
      >
        Board
        <i
          class="fa fa-th-large"
          aria-hidden="true"
        />
      </router-link>
      <router-link
        to="/backlog"
        :class="buttonClass('/backlog')"
      >
        Backlog
        <i
          class="fa fa-list"
          aria-hidden="true"
        />
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MenuBar',
  methods: {
    buttonClass(path) {
      return {
        btn: true,
        'btn-primary': this.$route.path === path,
        'btn-secondary': this.$route.path !== path
      };
    }
  }
};
</script>

<style>
.menubar {
  margin-bottom: 16px;
}
</style>

// The menu bar is the header of the app 
// contains the routes to the board and the backlog page to add tasks
// Buttons for navigation and text display