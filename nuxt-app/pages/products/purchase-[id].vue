<script setup>
const { id } = useRoute().params;
const response = await useFetch(`/api/products`);
const productData = toRaw(response.data.value);
const product = productData.find(item => item.id === id);
</script>

<template>
<section>
  <h1>Congratulations</h1>
  <h2>You Purchased our {{ product.title }}</h2>
</section>
</template>

<style lang="scss" scoped>
  section {
    height: 120vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 1000;
    color: black;
    background-color: #9fcbaa;
    font-size: sans-serif;
  }

  a {
    text-decoration: none;
  }
</style>