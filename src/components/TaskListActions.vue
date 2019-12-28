<template>
    <DetailsDropdown style="position: absolute;top: 12px;right: 10px;" ref="dropdown">
        <template v-slot:handle
        >...</template>

        <template v-slot:content>
            <label class="content-item" @click="showListEditPopup">Edit</label>
            <label class="content-item" @click="showArchiveListPopup">Archive</label>
    </template>
    </DetailsDropdown>
    </template>

    //The Edit action allows user to edit list details and archive action allows the user to archive the list
    //The responsibility of TaskListArchive component is to show a popup to confirm list archive action.