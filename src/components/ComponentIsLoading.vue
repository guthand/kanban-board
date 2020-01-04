<template>
    <div class="indcator text-center" v-if="is-Loading">
        <svg width="135" height="140" viewBox="0 0 135 140" xmlns="location of the svg" fill="#dc3545">
        </svg>
        <h4> Loading...</h4>
    </div>
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

//The mapGetters helper simply maps store getters to local computed properties:
//svg tag you set the width height and the location of the folder and color fill