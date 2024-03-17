<script setup>
const response = await useFetch('/api/links')
const linksData = toRaw(response.data.value)
</script>

<template>
  <NavBar :links="linksData"/>
  <NuxtPage />
</template>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-color: white;
  color: black;
  height: 200vh;
}
</style>
