<template>
  <article class="has-background-white-bis">
    <section class="mt-6 pt-6 pb-6">
      <div class="container">
        <div class="columns is-multiline">
          <div v-for="p in products" :key="p" :class="columnClasses">
            <ProductCard :product="p" />
          </div>
        </div>
      </div>
    </section>
  </article>
</template>

<script setup>
import { ref, computed } from "vue";
//  fetch the products
const { data: products } = await useFetch("https://fakestoreapi.com/products");
// definePageMeta({
//   layout: "products",
// });
useHead({
  title: "Nuxt Dojo | Merch",
  meta: [{ name: "description", content: "Nuxt 3 Merch" }],
});
const maxColumns = 4;

const columnClasses = computed(() => {
  const numColumns = Math.min(products.value.length, maxColumns);
  return `column is-${12 / numColumns}`;
});
</script>

<style></style>
