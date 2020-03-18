<template>
  <div class="alert alert-primary" :class="{'done': doneTask}">
    <button class="btn btn-primary btn-sm" @click="doneTask = !doneTask">√</button>
    {{ task }}
  </div>
</template>

<script>
export default {
  props: ['task'],
  data () {
    return {
      doneTask: false
    }
  }
}
</script>

<style>

  .done {
    text-decoration: line-through;
    color: gray;
  }
</style>
