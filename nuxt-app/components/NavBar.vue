<script setup>
import {ref} from 'vue'
const props = defineProps({
  links: {
    type: Array,
    required: true
  }
})
let isVisible = ref(false);
</script>

<template>
  <nav>
    <p style="color: white;">LOGO</p>
    <ul>
      <li v-for="({title, href}, i) in props.links" :key="i"><a :href="href">{{ title }}</a></li>
    </ul>
  <div @click="isVisible = !isVisible" class="menu-wrapper">
  <HamburguerMenu />
  </div>
  </nav>
  <ToggleMenu :isVisible="isVisible" :links="links" />
</template>

<style lang="scss" scoped>
nav {
 display: flex;
 justify-content: space-between;
 align-items: center;
 background-color: #BCB88A;
 width: 100%;
 position: sticky;
 top: 0;
 padding: 1rem;
}

ul {
  list-style-type: none;
  display: none;
  gap: 2.2rem;
  align-items: center;
}

li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

@media screen and (min-width: 880px) {
  ul {
    display: flex;
  }

  .menu-wrapper {
    display: none;
  }
}
</style>