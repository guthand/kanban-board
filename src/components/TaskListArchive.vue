<template>
    <DetailsPopup style="position:absolute;top: 12px; right: 10px;" ref="popup">
        <template v-slot:content v-if="board && list">
            <h3>Do you want to archive {{list.name}} list? </h3>
            <button class="btn btn-sm btn-danger" @click="handleTaskListArchive(list)">
                Yes, of course
            </button>
        </template>
    </DetailsPopup>
</template>

//If the user clicks on “Yes, of course"  button then archiveTaskList Vuex action is called to archive the list.