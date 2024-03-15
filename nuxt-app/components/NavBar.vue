<script setup>
import { ref } from "vue";
const props = defineProps({
  links: {
    type: Array,
    required: true,
  },
});
let isVisible = ref(false);
</script>

<template>
  <nav>
    <h1>TC</h1>
    <ul>
      <li v-for="({ title, href }, i) in props.links" :key="i">
        <NuxtLink :to="href">{{ title }}</NuxtLink>
      </li>
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
  background-color: #465e4c;
  width: 100%;
  position: absolute;
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

h1 {
  font-size: 2rem;
  color: white;
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