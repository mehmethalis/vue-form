<template>
  <div>
    <div class="form">
      <form action="">
        <label for="">Name</label><br />
        <input type="text" v-model="form.name" placeholder="Name" /><br />
        <label for="">Surname</label><br />
        <input type="text" v-model="form.lastname" placeholder="Surname" /><br />
        <label for="email">Email</label><br />
        <input type="text" v-model="form.email" placeholder="Email" /><br />
        <label for="phone">Phone</label><br />
        <input
          type="tel"
          v-model="form.phone"
          id="phone"
          name="phone"
          pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"
          placeholder="Your number"
        /><br />
        <label for="">City</label><br />
        <input type="text" v-model="form.city" placeholder="City" /><br />
        <label for="">District</label><br />
        <input type="text" v-model="form.district" placeholder="District" />

        <div class="checkbox">
          <input type="checkbox" v-model="form.isAgree" id="policy" name="policy" value="true" />
          <label for="policy">I agree to <a href="#" @click="setShow">Privacy Policy</a></label>
        </div>
        <button type="button" class="btn" @click="submit">Submit</button>
      </form>
    </div>
    <Popup v-if="isShow" @setShow="setShow" />
  </div>
</template>

<script>
import Popup from "./Popup.vue";

export default {
  name: "Form",
  data() {
    return {
      isShow: false,
      form: {
        name: "",
        lastname: "",
        phone: "",
        email: "",
        city: "",
        district: "",
        isAgree: false,
      },
    };
  },
  methods: {
    setShow() {
      this.isShow = !this.isShow;
    },
    submit() {
      let filtered = Object.keys(this.form)
        .filter((key) => ["name", "lastname", "phone", "email", "city", "district"].includes(key))
        .reduce((obj, key) => {
          obj[key] = this.form[key];
          return obj;
        }, {});

      filtered = { id: parseInt(Math.random()*100) , ...filtered };
      this.$emit("submit", filtered);
    },
  },
  components: {
    Popup,
  },
  props: {},
};
</script>

<style scoped>
.form {
  width: 350px;
}
.btn {
  width: 100%;
  padding: 15px 25px;
  border: none;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all ease-in-out 0.3s;
}
.checkbox {
  display: flex;
  padding: 10px 5px;
  gap: 10px;
}
input {
  padding: 7px;
  border-radius: 5px;
  border: solid 2px black;
  outline: none;
  transition: all ease-in-out 0.3s;
  margin-bottom: 15px;
}
input[type="text"],
input[type="tel"] {
  width: 100%;
}

input:focus {
  border-color: gray;
}

label {
  font-weight: 700;
  font-family: "Poppins", sans-serif;
}
</style>
