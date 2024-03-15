<script setup>
const props = defineProps({
  isVisible: {
    type: Boolean,
    required: true
  },

  links: {
    type: Array,
    required: true
  }

})
</script>

<template>

<div v-show="props.isVisible" class="toggle-menu">
      <ul class="toggle-items">
      <li v-for="({title, href}, i) in props.links" :key="i"><NuxtLink :to="href" class="link" @click="isVisible = !isVisible">{{ title }}</NuxtLink></li>
      </ul>
    </div>

</template>

<style lang="scss" scoped>
.toggle-menu {
  position: absolute;
  margin-top: 75px;
  height: 340px;
  transition: 0.4s;
  width: 100%;
  background-color: #465e4c;
  z-index: 1;
  animation: slideIn 0.3s ease forwards;
 }

 .link {
  display: block;
  width: 100%;
  height: 100%;
  padding-top: 20px;
 }

 .toggle-items {
  height: 100%;
  list-style-type: none;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly
 }

 li {
  display: block;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: 0.4s;
  cursor: pointer;
 }

 li:hover {
  background-color: white;
 }

 li:hover a {
  color: black
 }

 li a {
  text-decoration: none;
  color: white;
  font-size: 2rem;
  font-weight: bold;
 }

 @media screen and (min-width: 880px) {
  .toggle-menu {
    display: none;
  }
 }

 @keyframes slideIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
