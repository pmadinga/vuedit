<template>
  <div class="backdrop">
    <div class="modal">
      <h1>{{ header}}</h1>
      <p>Modal Content</p>
    </div>
  </div>
</template>

<script>
  export default{
    props: [ 'header' ],
  }
</script>

<style scoped>
  .modal{
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #fff;
    border-radius: 10px;
  }
  .backdrop{
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
  }
  h1{
    border: none;
    color: rgb(22, 119, 87);
  }
  p{
    font-style: normal;
  }
</style>