<template>
  <section class="header">
    <div class="header-content">
      <h1>{{ heroMessage }}</h1>

      <NuxtLink to="/products">
        <button class="button">Explore More</button>
      </NuxtLink>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const heroMessage = ref("Tech Crew");
const isVisible = ref(true);
</script>

<style scoped>
.header {
  background-image: url("https://i.gifer.com/83WF.gif");
  background-size: cover;
  background-position: center;
  height: 700px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-content {
  text-align: center;
  color: white;
  font-size: 50px;
}

.button {
  background-color: #9fcbaa;
  border: none;
  color: black;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 16px;
}

.button:hover {
  background-color: #1c3422;
  color: white;
  cursor: pointer;
}

@media (max-width: 768px) {
  .header-content {
    flex-direction: column;
  }
}
</style>
