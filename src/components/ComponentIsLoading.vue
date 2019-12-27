<template>
    <div class="indcator text-center" v-if="is-Loading">
        <svg width="" height="" viewBox="0 0 135 140" xmlns="location of the photo" fill="color">
        </svg>
</template>
<script>
import {mapGetters} from "vuex"
export default {
    computed:{
        ...mapGetters({
            isLoading:"isLoading"
        })
    }
}
</script>