<template>
 <h1>{{title}}</h1>
 <teleport to=".modals" v-if="showModal">
   <Modal header = "Signup for the given data !!"
    text="texting the data" @close="toggleModal"/>

  </teleport>
  <button @click="toggleModal">Open Modal</button>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Modal from './components/Model.vue'

export default {
  name: 'App',
  components: {Modal},
 data(){
  return {
    title: "My first vue projects",
    showModal:false
  }
 },

  methods: {
    handleClick(){
      console.log(this.$refs.name.value);
    },

    toggleModal(){
      this.showModal =!this.showModal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
