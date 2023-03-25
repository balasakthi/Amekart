<template>
  <div class="card">
    <nav class="breadcrumb pl-5 pt-5" aria-label="breadcrumbs">
      <ul>
        <li><NuxtLink to="/products">View all</NuxtLink></li>
        <li class="is-active">
          <a class="is-capitalized" href="#" aria-current="page">{{
            product.category
          }}</a>
        </li>
      </ul>
    </nav>
    <div class="columns">
      <div class="column has-text-centered">
        <img :src="`${product.image}`" class="p-6" />
      </div>
      <div class="column p-6">
        <h2 class="title is-size-3">{{ product.title }}</h2>
        <p class="is-size-5">Price - &#x20B9; {{ product.price }}</p>
        <h3 class="has-text-weight-bold mt-5">Product description:</h3>
        <hr class="mt-1" />
        <p class="mb-5">{{ product.description }}</p>
        <button class="button is-primary">
          <i class="fa-solid fa-cart-shopping pr-3"></i>
          <span>Add to cart</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style scoped>
img {
  max-width: 400px;
}
</style>
