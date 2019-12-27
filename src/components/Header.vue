<template>
    <nav class="navbar navbar-light bg-faded">
        <router-link to="/" class="navbar-brand">
        <label>
            Guthand board
            <span class="text-uppercase" v-show="this.activeBoard"> : {{ boardName }} </span>
        </label> 
        </router-link>
    </nav>
</template>

<script>
export default {
    name: 'Header'
}
</script>