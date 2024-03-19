<script setup>
const response = await useFetch('/api/products')
const productData = toRaw(response.data.value)
</script>

<template>
<article>
<h4>{{ productData[0].title }}</h4>
<figure>
  <img src="../assets/nintendo.jpg" :alt="productData[0].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[1].title }}</h4>
<figure>
  <img src="../assets/photo.jpg" :alt="productData[1].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[2].title }}</h4>
<figure>
  <img src="../assets/computer.jpg" :alt="productData[2].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[3].title }}</h4>
<figure>
  <img src="../assets/mouse.jpg" :alt="productData[3].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[4].title }}</h4>
<figure>
  <img src="../assets/smart.jpg" :alt="productData[4].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[5].title }}</h4>
<figure>
  <img src="../assets/headphones.jpg" :alt="productData[5].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[6].title }}</h4>
<figure>
  <img src="../assets/external.png" :alt="productData[6].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[7].title }}</h4>
<figure>
  <img src="../assets/router.jpg" :alt="productData[7].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[8].title }}</h4>
<figure>
  <img src="../assets/smartwatch.jpg" :alt="productData[8].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[9].title }}</h4>
<figure>
  <img src="../assets/printer.jpg" :alt="productData[9].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[10].title }}</h4>
<figure>
  <img src="../assets/bluetooth.jpg" :alt="productData[10].title" height="200" width="200">
</figure>
</article>

<article>
<h4>{{ productData[11].title }}</h4>
<figure>
  <img src="../assets/gaming.jpg" :alt="productData[11].title" height="200" width="200">
</figure>
</article>
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

img {
  display:block
}
</style>