<template>
  <div class="card task-lane-item">
    <div class="card-block">
        <h5 class="card-title">
            <span class="text-muted">#{{item.id}}</span>
            {{item.text}}
        </h5>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskLaneItem',
  props: ['item'],
};
</script>

<style>
.card.task-lane-item {
  background: #da240c;
}
</style>

// definition of the laneItem
// it is the component that can go from lane to lane
// item passed as props to the list
// its id is going according to the time of creation