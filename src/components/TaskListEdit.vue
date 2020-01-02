//The responsibility of this component is to show a popup with the form to update list name.
<template>
    <DetailsPopup ref="newListPopup" v-show="this.activeBoard" @popup-toggled="handlePopupToggled">
        <template v-slot:handle>
            <span class="nav-item btn btn-sm btn-app mr-2"> Add new List </span>
        </template>
        <template v-slot:content>
        <form>
            <h4>{{ heading }} </h4>
            <input 
                name="listName"
                type="text"
                class="form-control my-1"
                v-model.trim="listForm.name"
                v-validate="'required'"
                data-vv-as="List Name"
                placeholder="Enter your list name"
                />
                <small class="text-danger" style="display:block">{{ errors.first("listName") }}</small>
                <button class="btn btn-sm btn-app mt-2" @click.prevent="handleTaskListSave">
                    Save list
                </button>
        </form>
            </template>
    </DetailsPopup>
</template>