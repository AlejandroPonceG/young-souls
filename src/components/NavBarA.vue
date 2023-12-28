<script lang="ts">
import { defineComponent } from "vue";
import SideBar from "./SideBar.vue";

export default defineComponent({
  name: "NavBarA",
  components: {
    SideBar,
  },
  setup() {
    return {};
  },
});
</script>

<template>
  <div class="Navbar-base-box px-5">
    <div class="logo-section">
      <img class="nav-img" src="../../public/ys-icons/BG-2x-ico.png" alt="" />
      <div class="mx-2">
        <span class="text-dark image-text">Young Souls.</span>
      </div>
    </div>
    <div class="routes-section">
      <div><span class="fw-medium routes-text">Conócenos</span></div>
      <div><span class="fw-medium routes-text">Contáctanos</span></div>
    </div>
    <div class="buttons-section">
      <b-button variant="primary" class="btn-dark mx-3 py-3"
        v-b-toggle.sidebar-no-header><span>PRODUCTOS</span></b-button
      >
      <b-icon-whatsapp class="text-dark fs-1 w-icon"></b-icon-whatsapp>
    </div>
    <div class="list-menu-trigger" v-b-toggle.sidebar-no-header>
      <b-icon-list class="fs-1"></b-icon-list>
    </div>
    <SideBar />
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
  justify-content: space-between;
}

.logo-section {
  display: flex;
  align-items: center;
}
.buttons-section {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.nav-img {
  width: 45px;
}

.routes-section {
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

.list-menu-trigger {
  display: none;
}

@media only screen and (min-device-width: 375px) and (max-device-width: 700px) {
  .image-text {
    display: none;
  }

  .buttons-section {
    display: none;
  }

  .routes-section {
    display: none;
  }

  .list-menu-trigger {
    display: block;
  }
}
</style>
