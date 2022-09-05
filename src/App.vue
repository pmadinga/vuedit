<template>
  <h1>{{ title }}</h1>
  <br>

  <p>Welcome</p>
  <teleport to=".modals" v-if="showModal">
    <Modal theme='sale' @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up now</a>
        <a href="#">More info</a>
      </template>
      <h1>Open Modal</h1>
      <p>This is an open modal</p>
    </Modal>
  </teleport>
  <teleport to=".modals" v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <template v-slot:links>
        <a href="#">Sign up now</a>
        <a href="#">More info</a>
      </template>
      <h1>Modal 2 open</h1>
      <p>This is another open modal</p>
    </Modal>
  </teleport>
  <button @click.alt="toggleModal" >Open Modal (alt)</button>
  <button @click="toggleModalTwo">Open second modal</button>
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
      title: 'First Vue App',
      showModal: false,
      showModalTwo: false,
    }
  },   
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    },
    toggleModalTwo(){
      this.showModalTwo = !this.showModalTwo
    }
  }
}
</script>

<style>
  *{
    margin: 0;
  }
  #app, .modals {
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
