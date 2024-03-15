<script setup>
const props = defineProps({
  products: {
    type: Array,
    required: true
  }
})
</script>

<template>
<article v-for="({title,description,image},i) in props.products" :key="i">
<h4>{{ title }}</h4>
<figure>
  <img src="../assets/nintendo.jpg" :alt="title" height="150" width="150">
</figure>
</article>
</template>

<style lang="scss" scoped>
article {
  height: 340px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  border: 2px solid black;
}

img {
  display:block
}
</style>