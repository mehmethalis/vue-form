<template>
    <div class="modal-backdrop">
        <div class="modal-popup">
            <div class="modal-header">
                <h1>Policy</h1>
                <button @click="$emit('setShow')" class="btn">Close X</button>
            </div>
            <div class="modal-body">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam beatae maiores, minima
                possimus vero exercitationem voluptates iusto libero hic culpa, ex deleniti eaque nobis quisquam illo unde
                porro ut atque neque repudiandae. Maxime ipsum aspernatur esse dolorem facilis blanditiis, reiciendis ullam
                at animi, dolor sint est nemo officiis sequi fugit laborum nostrum! Tempora enim vel, a excepturi odio
                ratione eaque nulla, esse unde similique cumque sapiente architecto, libero dolore est voluptatum. Expedita
                ea ullam amet repellat numquam minus eos fugit reiciendis impedit ad natus incidunt eius, deleniti totam
                voluptatem ex sed. Atque veritatis reprehenderit quia labore, incidunt expedita reiciendis fuga rem neque
                vel, perferendis eius ullam deserunt praesentium blanditiis. Quo fuga dolore unde officia debitis provident
                quia inventore voluptates consequuntur, ipsum eveniet assumenda explicabo amet quam! Magni consequuntur
                obcaecati accusamus fuga minus nulla? Autem pariatur dolores quia debitis voluptatum veritatis explicabo
                porro dolorum corporis sequi, dicta magni incidunt nisi nostrum aperiam, sint magnam non! Porro sequi beatae
                voluptates ab eaque incidunt odio! Ex excepturi a rem odit quidem doloribus eos officiis velit. Perferendis
                voluptates modi debitis iste alias labore sunt. Doloremque vel laborum ipsa tempora recusandae eum expedita
                officiis provident molestiae nobis unde mollitia commodi quos ut, optio modi aliquid perferendis voluptatem,
                debitis illum odit. Et dignissimos cum repudiandae sunt. Mollitia, voluptate illo tempore suscipit obcaecati
                quam excepturi culpa deserunt, minima iure consequuntur. Neque, sequi quibusdam sit commodi saepe sapiente!
                Laudantium laborum nam quam blanditiis nostrum ea esse suscipit similique non ratione nulla quidem,
                obcaecati ullam adipisci ad numquam corrupti!</div>
        </div>
    </div>
</template>
   
<script>
export default {
    name: 'Popup',
    props: {

    }
}
</script>
   
<style>
.modal-backdrop {
    position: absolute;
    height: 100vh;
    background: rgba(0, 0, 0, 0.2);
    z-index: 2;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.modal-popup {
    background: #fff;
    width: 500px;
    border-radius: 10px;
    padding: 20px;
}

.modal-header {
    display: flex;
    justify-content: space-between;
}

.modal-body {
    height: 500px;
    overflow-y: scroll;
    overflow-x: hidden;
    padding: 20px;
}
</style>
   