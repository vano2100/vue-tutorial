<template>
  <div id="app">
    <h2>My to-do list</h2>
    <div class="form-group mb-2">
      <label for="taskName" class="col-sm-2 col-form-label">Название задачи:</label>
      <input class="form-control" type="text" v-model="newName" id="taskName">
    </div>
    <button class="btn btn-primary  mb-2" @click="addItem">Добавить задачу</button>
    <hr>

    <div class="tasks">
      В работе
      <app-item
      v-for="task in tasks"
      v-bind:task="task"
      ></app-item>
    </div>

  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  name: 'app',
  data () {
    return {
      tasks: [],
      newName: ''
    }
  },
  methods: {
    addItem: function(){
      this.tasks.push(this.newName)
      this.newName = ''
    }
  },
  components: {
    appItem: Item
  }
}
</script>

<style>

</style>
