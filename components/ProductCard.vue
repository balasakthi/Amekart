<template>
  <div class="card has-text-centered">
    <figure class="p-5">
      <img :src="`${product.image}`" />
    </figure>

    <div class="card-content pt-0">
      <div class="content">
        <div class="product-title is-clipped">
          <h2 class="title is-size-5">{{ product.title }}</h2>
        </div>
        <NuxtLink
          :to="`/products/${product.id}`"
          class="button is-primary is-rounded mb-2 mt-3"
        >
          View Details
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped>
.product-title {
  height: 1.5rem;
  margin-bottom: 1rem;
}
img {
  max-height: 130px;
}
</style>
