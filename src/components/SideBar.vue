<script lang="ts">
import { defineComponent, ref } from "vue";
import CategoryCard from "./CategoryCard.vue";

export default defineComponent({
  name: "SideBar",
  components: { CategoryCard },

  data() {
    const categories = ref([
      {
        image: "../../public/images/ropa.webp",
        title: "Oversize",
        subtitle: "Camisetas",
      },
      {
        image: "../../public/images/ropa.webp",
        title: "Cargo",
        subtitle: "Pantalones",
      },
      {
        image: "../../public/images/ropa.webp",
        title: "Jeans",
        subtitle: "Pantalones",
      },
      {
        image: "../../public/images/ropa.webp",
        title: "YScaps",
        subtitle: "Gorras",
      },
    ]);

    const screenWidth = ref(window.screen.width);

    return {
      categories,
      screenWidth,
    };
  },

  methods: {
    showProducts(id: string) {
      this.$router.push('/'+id)
    },
  },
});
</script>

<template>
  <b-sidebar
    id="sidebar-no-header"
    aria-labelledby="sidebar-no-header-title"
    no-header
    shadow
    right
  >
    <template #default="{ hide }">
      <div class="close-header-box p-4">
        <button
          type="button"
          class="btn-close"
          aria-label="Close"
          @click="hide"
        ></button>
      </div>
      <div class="p-3">
        <div v-if="screenWidth <= 600" class="routes-section-box p-2">
          <a>
            <b-icon-chevron-right
              style="font-size: 5px !important; width: 12px"
            ></b-icon-chevron-right>
            <span class="pointer">Conócenos</span></a
          >
          <a>
            <b-icon-chevron-right
              style="font-size: 5px !important; width: 12px"
            ></b-icon-chevron-right>
            <span class="pointer">Contáctanos</span></a
          >
        </div>
        <hr v-if="screenWidth <= 600" />
        <div class="categories-section-box p-2">
          <h3 class="fw-bolder">Categorías</h3>
          <div
            v-for="(category, idx) in categories"
            :key="idx"
            class="category-card-section"
            @click="showProducts(category.title)"

          >
            <CategoryCard
              :image="category.image"
              :title="category.title"
              :subtitle="category.subtitle"
            />
          </div>
        </div>
      </div>
    </template>
  </b-sidebar>
</template>

<style>
.category-card-section {
  width: 100%;
}

.category-card-section:hover {
  cursor: pointer;
  transform: scale(1.05);
}

.close-header-box {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.routes-section-box {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

.categories-section-box {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

h2 {
  font-weight: 700;
}

a {
  color: black;
  text-decoration: none;
}

.close-icon:hover {
  cursor: pointer;
}
</style>
