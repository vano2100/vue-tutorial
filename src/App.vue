<template>
  <div id="app">
    <h2>My to-do list</h2>
    <input type="text" v-model="newName">
    <button @click="addItem">add</button>
    <hr>

    <div class="items">
      <app-item 
      v-for="itemCaption in itemCaptions"
      v-bind:itemCaption="itemCaption"
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
      itemCaptions: ['item1'],
      newName: ''
    }
  },
  methods: {
    addItem: function(){
      this.itemCaptions.push(this.newName)
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
