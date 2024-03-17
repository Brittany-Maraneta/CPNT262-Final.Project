<script setup>
const response = await useFetch('/api/products')
const productData = toRaw(response.data.value)
</script>

<template>
<section>
  <Card :products="productData" />
</section>
</template>

<style lang="scss" scoped>
section {
  display: grid;
  grid-template-columns: repeat(4,1fr);
}
</style>