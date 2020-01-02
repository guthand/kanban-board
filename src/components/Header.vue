<template>
    <nav class="navbar navbar-light bg-faded">
        <router-link to="/" class="navbar-brand">
        <label>
            Guthand board
            <span class="text-uppercase" v-show="this.activeBoard"> : {{ boardName }} </span>
        </label> 
        </router-link>
        <div class="d-flex justify-content-end" v-if="!ComponentIsLoading">
            <TaskListRestore></TaskListRestore>
            <TaskListEdit></TaskListEdit>
            <TaskBoardEdit></TaskBoardEdit>
            <TaskListArchive></TaskListArchive>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Header'
}
</script>