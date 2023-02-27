<template>
    <div>
        <h1>Form</h1>
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
   
<style></style>
   