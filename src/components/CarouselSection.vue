<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "CarouselSection",
  setup() {
    return {};
  },
});
</script>

<template>
  <div class="py-5 px-5">
    <b-row class="align-items-center">
      <b-col class="left-column text-start">
        <div class="py-3">
          <span class="left-title-text"
            >Integrate your stack -> automate your work</span
          >
        </div>
        <div class="py-3">
          <span class="left-complement-text"
            >Envolve at the speed and scale of your business with the leader in
            low-code automation</span
          >
        </div>
        <div class="py-3">
          <b-button variant="primary" class="btn-dark py-3"
            ><span>PRODUCTOS</span></b-button
          >
          <b-button variant="primary" class="btn-light py-3 mx-4"
            ><b-icon-whatsapp class="text-success"></b-icon-whatsapp
            ><span class="text-dark mx-2">WhatsApp</span></b-button
          >
        </div>
        <div class="py-3 text-secondary">&#169; Young Souls 2024</div>
      </b-col>
      <b-col class="py-2">
        <div class="image-box">
          <div class="image-section"></div>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<style>
.left-title-text {
  color: #000;
  font-family: Inter;
  font-size: 96px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.left-complement-text {
  color: #000;
  font-family: Inter;
  font-size: 32px;
  font-style: normal;
  font-weight: 300;
  line-height: normal;
}

.image-box {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-section {
  min-width: 280px;
  width: 100% !important;
  height: 800px;
  background-image: url("../../public/images/prueba2.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  border-radius: 35px;
}
</style>
