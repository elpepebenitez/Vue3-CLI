<template>
  <h1>{{ title }}</h1>
  <modal :header="header" :text="text" theme="sale"></modal>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  data() {
		return {
      title: 'My first vue 3 app :)',
      header: 'Sign Up!',
      text: 'Don\'t miss out on this opportunity!'
		}
	},
  components: {
    Modal
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
