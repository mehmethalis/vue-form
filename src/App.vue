<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <Form />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Form
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  position: relative;
}

.container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 100px;
}
</style>
