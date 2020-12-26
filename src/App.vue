<template>
  <h1>{{ title }}</h1>
  <p>Welcome</p>
  
  <teleport to=".modals" v-if="showModal">
    <modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up now</a>
        <a href="#">More info</a>
      </template>
      <h1>Giveaway!</h1>
      <p>Grab yours for half price!</p>
    </modal>
  </teleport>

  <button @click="toggleModal" >Open Modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  data() {
		return {
      title: 'My first vue 3 app :)',
      header: 'Sign Up!',
      text: 'Don\'t miss out on this opportunity!',
      showModal: false
		}
	},
  components: {
    Modal
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
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
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
