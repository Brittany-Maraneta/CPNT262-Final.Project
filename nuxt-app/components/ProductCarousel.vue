<script setup>
import { ref, onMounted, onBeforeUnmount, computed } from 'vue';
let indexNumber = ref(0);
let interval;
const bannerImageArray = [
{
  title: 'Buy A Computer',
  src: 'com.jpg'
},

{
  title: 'Get A Brand New Nintendo Switch',
  src: 'switch.jpg'
},

{
  title: 'Get Your Own Camera',
  src: 'camera.webp'
},

{
  title: 'Buy The Best New Mouse',
  src: 'mouse.jpg'
}
];

const slideChange = () => {
interval = setInterval(() => {
    indexNumber.value = (indexNumber.value + 1) % bannerImageArray.length;
  },3500)
}

onMounted(() => {
  slideChange();
});

onBeforeUnmount(() => {
  clearInterval(interval);
});

const title = computed(() => {
 return bannerImageArray[indexNumber.value].title
})
const bannerImage = computed(() => {
 return `banner${indexNumber.value}`
})

</script>

<template>
  <header :class="bannerImage">
  <section>
  <h2>{{ text }}</h2>
  <Button>{{ title }}</Button>
  </section>
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 90vh;
  margin-top: 32px;
  background-size: cover;
  background-position: center; 
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: opacity 0.5s ease;
}

.banner0 {
  background-image: url(../public/pexels.jpg);
}

.banner1 {
  background-image: url(../public/switch.jpg);
}

.banner2 {
  background-image: url(../public/camera.webp);
}

.banner3 {
  background-image: url(../public/mouse.jpg);
}
</style>