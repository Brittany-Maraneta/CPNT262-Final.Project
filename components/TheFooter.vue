<script setup>
const response = await useFetch("/api/links");
const mediaResponse = await useFetch("/api/socialMediaLinks");
const footerResponse = await useFetch("/api/footerLinks");
const linkData = toRaw(response.data.value);
const mediaData = toRaw(mediaResponse.data.value);
const footerData = toRaw(footerResponse.data.value);
</script>

<template>
  <section class="footer">
    <img src="../public/logo.svg" alt="logo" />
    <ul class="nav-links">
      <li v-for="({ title, href }, i) in linkData" :key="i">
        <a :href="href">{{ title }}</a>
      </li>
    </ul>
    <ul class="social-links">
      <li v-for="({ icon, title }, i) in mediaData" :key="i">
        <a href="#" :title="title"><Icon class="icon" :name="icon" /></a>
      </li>
    </ul>
    <ul class="links">
      <li v-for="({ name }, i) in footerData" :key="i">{{ name }}</li>
    </ul>
    <p>Get Busy @ Tech Crew © 2024 Calgary AB</p>
  </section>
</template>

<style lang="scss" scoped>
section {
  height: 80vh;
  background-color: #465e4c;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 1rem;
  text-align: center;
  gap: 2.2rem;
  font-family: Arial, Helvetica, sans-serif;
}

img {
  margin-bottom: 2rem;
}

.links {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 100%;
  cursor: pointer;
}

.nav-links {
  display: flex;
  justify-content: center;
  gap: 1.2rem;
  width: 100%;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
  width: 100%;
}

a {
  color: white;
  text-decoration: none;
}

.icon {
  font-size: 2rem;
  transition: 0.4s;
}

.icon:hover {
  color: rgba(255, 255, 255, 0.6);
}

ul {
  list-style-type: none;
}

.links li {
  color: white;
  text-decoration: none;
  transition: color 0.4s;
}

.links li:hover {
  color: #1c3422;
  cursor: pointer;
}

.nav-links a {
  color: white;
  text-decoration: none;
  transition: color 0.4s;
}

.nav-links a:hover {
  color: #1c3422;
  cursor: pointer;
}

.footer img:hover {
  transform: scale(1.2);
  transition: transform 0.4s;
}
</style>
