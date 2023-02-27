<template>
  <nav class="navbar">
    <div class="left">Logo</div>
    <div class="right">User</div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: {

  }
}
</script>

<style>
.navbar {
  background: #3A1078;
  color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
}
</style>
