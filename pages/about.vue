<template>
  <section class="mt-6 pt-6">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet,
      explicabo quidem? Sunt vitae aperiam, quisquam accusantium sit impedit
      voluptatibus asperiores quo aliquid corrupti voluptates nemo nobis ab
      illum, unde consectetur.
    </p>
    <p>{{ data }}</p>
  </section>
</template>

<script setup>
const { data } = await useFetch("/api/ninja");
</script>

<style></style>
