<template>
  <Head>
    <Title>Nuxt Dojo | {{ product.title }}</Title>
    <Meta name="description" :content="product.description" />
  </Head>

  <section class="mt-6 pt-6 has-background-white-bis" style="height: 100vh">
    <div class="container"><ProductDetails :product="product" /></div>
  </section>
</template>

<script setup>
const { id } = useRoute().params;
const uri = "https://fakestoreapi.com/products/" + id;
//  fetch the products
const { data: product } = await useFetch(uri, { key: id });
if (!product.value) {
  throw createError({ statusCode: 404, statusMessage: "Product not found" });
}
// definePageMeta({
//   layout: "products",
// });
</script>

<style></style>
