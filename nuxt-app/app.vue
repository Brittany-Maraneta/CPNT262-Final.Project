<script setup>
const links = [
  {
    title: 'Home',
    href: '#'
  },

  {
    title: 'Products',
    href: '#'
  },

  {
    title: 'About',
    href: '#'
  },

  {
    title: 'Contact',
    href: '#'
  },
]
</script>

<template>
  <div>
    <NavBar :links="links" />
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box
}
</style>
