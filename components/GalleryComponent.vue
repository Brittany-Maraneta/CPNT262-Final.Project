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
  grid-template-columns: repeat(3,1fr);
}

@media screen and (max-width: 800px) {
  section {
    grid-template-columns: repeat(2,1fr);
  }
}

@media screen and (max-width: 600px) {
  section {
    grid-template-columns: repeat(1,1fr);
  }
}

</style>