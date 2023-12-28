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
  <div class="py-4 px-5">
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
        <div class="py-3 complement-buttons-box">
          <b-button variant="primary" class="btn-dark py-3"
            v-b-toggle.sidebar-no-header><span>PRODUCTOS</span></b-button
          >
          <b-button variant="primary" class="btn-light py-3 mx-4"
            ><b-icon-whatsapp class="text-success"></b-icon-whatsapp
            ><span class="text-dark mx-2">WhatsApp</span></b-button
          >
        </div>
        <div class="py-3 text-secondary copy">&#169; Young Souls 2024</div>
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

.complement-buttons-box {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

@media only screen and (min-device-width: 375px) and (max-device-width: 1000px) {
  .left-title-text {
    font-size: 56px;
  }

  .left-complement-text {
    font-size: 22px;
  }

  .complement-buttons-box {
    flex-direction: column;
    gap: 10px;
  }

  .copy {
    text-align: center;
  }

}

</style>
