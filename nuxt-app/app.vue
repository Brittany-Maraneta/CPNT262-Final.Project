<script setup>
import Header from "./components/Header.vue";

const links = [
  {
    title: "Home",
    href: "#",
  },

  {
    title: "Products",
    href: "#",
  },

  {
    title: "About",
    href: "#",
  },

  {
    title: "Contact",
    href: "#",
  },
];
</script>

<template>
  <div>
    <NavBar :links="links" />
  </div>
  <main>
    <Header />
    <section class="main-body">
      <MainHome />
    </section>
  </main>
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
