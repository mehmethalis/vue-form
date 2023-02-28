<template>
  <div id="app">
    <Navbar />
    <div class="container">
      <Form @submit="addUser"/>
      <List :columns="columns" :rows="rows" />
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Form from "./components/Form.vue";
import List from "./components/List.vue";

export default {
  name: "App",
  data() {
    return {
      columns: ["ID","First Name", "Last Name", "Email", "Phone", "City", "District"],
      rows: [
        {
          id: "1",
          firstName: "Mehmet",
          lastName: "Çiçek",
          email: "mehmet@halis.com",
          phone: "5342223344",
          city: "Balıkesir",
          district: "Ayvalık",
        },
        {
          id: "2",
          firstName: "Ali",
          lastName: "Mehmet",
          email: "ali@mehmet.com",
          phone: "5342223344",
          city: "İzmir",
          district: "Bayraklı",
        },
      ],
    };
  },
  methods:{
    addUser(user){
      console.log(user)
      this.rows.push(user)
    }
  },
  components: {
    Navbar,
    Form,
    List,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  position: relative;
}

.container {
  display: flex;
  align-items: flex-start;
  justify-content: space-around;
  margin-top: 100px;
}
</style>
