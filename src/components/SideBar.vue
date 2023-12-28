<script lang="ts">
import { defineComponent, ref } from "vue";
import CategoryCard from "./CategoryCard.vue";


export default defineComponent({
  name: "SideBar",
  setup() {
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
        title: "YS caps",
        subtitle: "Gorras",
      },
    ]);

    return {
      categories,
    };
  },
  components: { CategoryCard },
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
      <div class="close-header-box p-3" @click="hide">
        <b-icon-x class="close-icon fs-2"></b-icon-x>
      </div>
      <div class="p-3">
        <div class="routes-section-box p-2">
          <a> <b-icon-chevron-right style="font-size: 5px !important; width: 12px;"></b-icon-chevron-right> <span class="pointer">Conócenos</span></a>
          <a> <b-icon-chevron-right style="font-size: 5px !important; width: 12px;"></b-icon-chevron-right> <span class="pointer">Contáctanos</span></a>
        </div>
        <hr />
        <div class="categories-section-box p-2">
          <h3 class="fw-bolder">Categorías</h3>
          <div 
            v-for="(category, idx) in categories" 
            :key="idx" 
            class="category-card-section"
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
