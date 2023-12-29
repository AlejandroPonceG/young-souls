<!-- eslint-disable vue/multi-word-component-names -->
<script lang="ts">
import ProductsHeader from '@/components/ProductsHeader.vue';
import { defineComponent } from 'vue';
export default defineComponent({
    setup() {
        return {};
    },
    components: { ProductsHeader }
})

</script>
<template>
    <div class="main-box py-3 px-5">
        <ProductsHeader />
    </div>
</template>
<style></style>