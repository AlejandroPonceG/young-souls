<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'NavBarA',
  setup() {
    return {

    }
  }  
})
</script>

<template>
    <div class="Navbar-base-box px-5">
        <div class="logo-section">
            <img class="nav-img" src="../../public/ys-icons/BG-2x-ico.png" alt="">
            <div class="mx-2">
                <span class="text-dark image-text">Young Souls.</span>
            </div>
        </div>
        <div class="routes-section">
            <div><span class="fw-medium routes-text">Conócenos</span></div>
            <div><span class="fw-medium routes-text">Contáctanos</span></div>
        </div>
        <div class="buttons-section">
            <b-button variant="primary" class="btn-dark mx-3 py-3"><span>PRODUCTOS</span></b-button>
            <b-icon-whatsapp class="text-dark fs-1 w-icon"></b-icon-whatsapp>
        </div>
    </div>
</template>

<style>

.w-icon:hover {
    transform: scale(1.1);
    cursor: pointer;
}

.border { 
    border: 1px solid;
}

.routes-text {
    font-size: 20px;
}

.Navbar-base-box {
    width: 100%;
    height: 101px;
    display: flex;
    align-items: center;
}

.logo-section {
    width: 15%;
    display: flex;
    align-items: center;
}
.buttons-section {
    width: 15%;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}

.nav-img {
    width: 45px;
}

.routes-section {
    width: 70%;
    display: flex;
    align-items: center;
    gap: 30px;
}

.image-text {
    font-weight: 900;
    font-size: 24px !important;
}

.btn {
    min-width: 180px !important;
}

</style>