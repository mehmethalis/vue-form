<template>
    <div>

        <h1>Form</h1>
        <div>
            <form action="">
                <label for="">Name</label><br>
                <input type="text" placeholder="Name"><br>
                <label for="">Surname</label><br>
                <input type="text" placeholder="Surname"><br>
                <label for="phone">Enter your phone number</label><br>
                <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"
                    placeholder="Your number"><br>
                <label for="">City</label><br>
                <input type="text" placeholder="City"><br>
                <label for="">District</label><br>
                <input type="text" placeholder="District">
            </form>
        </div>
        <Popup v-if="isShow" @setShow="setShow" />
        <a href="#" @click="setShow">Open</a>
    </div>
</template>
   
<script>
import Popup from './Popup.vue'


export default {
    name: 'Form',
    data() {
        return {
            isShow: false
        }
    },
    methods: {
        setShow() {
            this.isShow = !this.isShow
        }
    },
    components: {
        Popup,
    },
    props: {

    }
}
</script>
   
<style>
input {
    width: 210px;
    padding: 7px;
    border-radius: 5px;
    border: solid 2px black;
}

label {
    font-weight: 700;
    font-family: 'Poppins', sans-serif;
}
</style>
   