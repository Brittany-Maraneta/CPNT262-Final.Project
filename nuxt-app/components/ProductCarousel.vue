<script setup>
let newItem;
const bannerImageArray = [
{
  title: 'Computer',
  src: '../public/computer.jpg'
},

{
  title: 'Nintendo Switch',
  src: '../public/switch.jpg'
},

{
  title: 'Camera',
  src: '../public/camera.webp'
},

{
  title: 'Mouse',
  src: '../public/mouse.jpg'
}
];

const carousel = (element) => {
  newItem = document.createElement('img');
  newItem.setAttribute('src', bannerImageArray[0].src);
  newItem.setAttribute('alt', bannerImageArray[0].title);
  element.appendChild(newItem)
  console.log(bannerImageArray[0].src)
}
</script>

<template>
  <figure :ref="carousel">
    <img src="../public/computer.jpg" alt="computer">
  </figure>
</template>

<style lang="scss" scoped>

</style>