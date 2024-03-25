<script setup>
const props = defineProps({
  products: {
    type: Array,
    required: true
  }
})
</script>

<template>
<NuxtLink v-for="({id,title,description,image},i) in props.products" :key="i" :to="`/products/product-${id}`" style="text-decoration: none;">
<article>
<h4>{{ title }}</h4>
<figure>
  <img :src="image" :alt="title" height="200" width="200">
</figure>
</article>
</NuxtLink>
</template>

<style lang="scss" scoped>
article {
  height: 340px;
  font-size: 1.5rem;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  border: 2px solid black;
  margin: 1rem;
  cursor: pointer;
  transition: 0.4s;
  background-color: #9fcbaa;
  border-radius: 10px;
}

article:hover {
  scale: 1.05;
}

a {
  color: black;
  font-family: sans-serif;
}

img {
  display:block
}
</style>