<template>
  <div id="main">
    <component :is="currentView"></component>
    <button @click="toggleView">toggle view</button>
  </div>
</template>

<style>
 #main {
   width: 200px;
   margin: auto;
   border-style: solid;
   border-color: blue;
   border-radius: 10px;
   border-width: 2px;
   padding: 10px;
 }
</style>

<script>
let views = {
  home: {
    template: '<p> this is home </p>'
  },
  posts: {
    template: '<p> this is posts </p>'
  },
  archive: {
    template: '<p> this is archive </p>'
  }
}

export default {
  data: function () {
    return {
      currentView: 'home'
    }
  },
  components: views,
  methods: {
    toggleView: function () {
      this.currentView === 'home' ?
        this.currentView = 'posts' :
        this.currentView = 'home'
    }
  }
}
</script>
