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
      <SwiperSlide>
        <img src="../public/com.jpg" :alt="bannerData[0].title">
      </SwiperSlide>

      <SwiperSlide>
        <img src="../public/switch.jpg" :alt="bannerData[1].title">
      </SwiperSlide>

      <SwiperSlide>
        <img src="../public/camera.webp" :alt="bannerData[2].title">
      </SwiperSlide>

      <SwiperSlide>
        <img src="../public/mouse.jpg" :alt="bannerData[3].title">
      </SwiperSlide>

      <!-- useSwiper() within a swiper instance -->
      <SwiperControls />
    </Swiper>
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
}
.swiper-wrapper {
  min-width: 100vh;
  width: 100%;
}

img {
  width: 100%;
  height: 100vh;
}

</style>