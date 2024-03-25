<script setup>
const { id } = useRoute().params;
const response = await useFetch(`/api/products`);
const productData = toRaw(response.data.value);
const {title,description,image,price} = productData.find(item => item.id === id);
</script>

<template>
<section>
<figure>
  <img :src="image" :alt="title">
</figure>
<article>
<h2>{{ title }}</h2>
<h4>${{ price }}</h4>
<p>{{ description }}</p>
<NuxtLink :to="`/products/purchase-${id}`">
<Button style="border: 2px solid #1c3422;">Buy Now</Button>
</NuxtLink>
</article>
</section>
<NuxtLink to="/products">
  <h5>Go Back</h5>
</NuxtLink>
</template>

<style lang="scss" scoped>
section {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1.3rem;
  height: 120vh;
  background-color: #9fcbaa;
  font-family: sans-serif;
}

img {
  width: 300px;
  height: 200px;
}

article {
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

p {
  max-width: 30ch;
  line-height: 1.5;
}

h5 {
  position: absolute;
  top: 20%;
  left: 10%;
  font-family: sans-serif;
  border: 2px solid #1c3422;
  color: black;
  border-radius: 20px;
  padding: 1rem;
  transition: 0.4s;
  cursor: pointer;
}

h5:hover {
  color: white;
  background-color: #1c3422;
}

@media screen and (max-width:800px) {
  section {
    flex-direction: column;
  }

  img {
    width:150px;
    height: 100px;
  }

  h5 {
    visibility: hidden;
  }
}
</style>