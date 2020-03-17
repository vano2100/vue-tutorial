<template>
  <div class="item" :class="{'done': doneTask}">
    <button @click="doneTask = !doneTask">V</button>
    {{ itemCaption }}
  </div>
</template>

<script>
export default {
  props: ['itemCaption'],
  data () {
    return {
      doneTask: false
    }
  },
  methods: {
    markDone: function(){
      doneTask = !doneTask
    }
  },
}
</script>

<style>

  .done {
    text-decoration: line-through;
    color: gray;
  }
</style>
