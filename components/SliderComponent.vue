<script setup>
const response = await useFetch('api/bannerProducts');
const bannerData = toRaw(response.data.value);
</script>

<template>
  <Swiper
      :height="300"
      :modules="[SwiperAutoplay, SwiperEffectCreative]"
      :slides-per-view="1"
      :loop="true"
      :effect="'fade'"
      :autoplay="{
        delay: 2000,
        disableOnInteraction: false
      }"
      :creative-effect="{
        prev: {
          shadow: false,
          translate: ['-20%', 0, -1]
        },
        next: {
          translate: ['100%', 0, 0]
        }
      }"
    >
      <SwiperSlide v-for="({id,src,title},i) in bannerData" :key="i">
        <img :src="src" :alt="title">
      </SwiperSlide>

      <div class="button-wrapper">
        <a href="#products">
        <Button>
          View All Our Products
        </Button>
        </a>
      </div>

    </Swiper>
    <GalleryComponent id="products" />
</template>

<style lang="scss" scoped>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  height: 20vh;
  font-size: 4rem;
  font-weight: bold;
  font-family: 'Roboto', sans-serif;
  width: 100%;
  height: 100%;
  cursor: pointer;
}
.swiper-wrapper {
  min-width: 100vh;
  width: 100%;
}

img {
  width: 100%;
  height: 100vh;
}

.button-wrapper {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 200;
}

</style>