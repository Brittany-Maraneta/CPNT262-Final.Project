<script setup>

const links = [
  {
    title: "Home",
    href: "/",
  },

  {
    title: "Products",
    href: "/products",
  },

  {
    title: "About",
    href: "/about",
  },

  {
    title: "Contact",
    href: "/contact",
  },
];
</script>

<template>
  <NavBar :links="links" />
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
