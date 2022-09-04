<template>
  <h1>{{ title }}</h1>
  <Modal 
    header='sign up for the giveaway'
    text="Grab your swafg for a half price"
  />
</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',
  components: {
    Modal
  },
  data(){
    return{
      title: 'First Vue App'
    }
  },   
  methods: {
    handleClick() {
      console.log(this.$refs.name.value);
      this.$refs.name.classList.add('active')
    }
  }
}
</script>

<style>
  *{
    margin: 0;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  h1{
    border-bottom: 1px solid #ddd;
    padding-bottom: 10px;
    display: inline-block;
  }
</style>
