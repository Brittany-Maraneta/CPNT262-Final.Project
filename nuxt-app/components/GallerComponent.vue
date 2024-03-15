<script setup>
const products = [
  {
    title: "Nintendo Switch",
    description: "Experience gaming like never before with the versatile Nintendo Switch. Seamlessly switch between handheld and console modes for gaming on the go or at home. Whether you're a Mario Kart enthusiast or a Legend of Zelda adventurer, the Switch offers endless entertainment.",
    image: "../assets/nintendo.jpg"
  },
  {
    title: "Camera",
    description: "Capture life's precious moments in stunning detail with a high-quality camera. From family gatherings to scenic landscapes, unleash your creativity and preserve memories with every click. Whether you're a beginner or a professional photographer, find the perfect shot with ease.",
    image: "https://example.com/camera_image.jpg"
  },
  {
    title: "Computer",
    description: "Power through work tasks, gaming sessions, and creative projects with a reliable computer. From sleek laptops to powerful desktops, find the perfect balance of performance and portability to suit your needs. Stay connected, organized, and productive with cutting-edge technology at your fingertips.",
    image: "https://example.com/computer_image.jpg"
  },
  {
    title: "Mouse",
    description: "Navigate with precision and efficiency using a high-performance mouse. Whether you're editing documents, browsing the web, or dominating in gaming competitions, find the perfect mouse tailored to your preferences. With ergonomic design and customizable features, enhance your productivity and gaming experience.",
    image: "https://example.com/mouse_image.jpg"
  },
  {
    title: "Smartphone",
    description: "Stay connected and productive on the go with a feature-packed smartphone. From seamless multitasking to stunning photography, unlock endless possibilities with the latest smartphone technology. Whether you're managing emails, capturing memories, or staying entertained, find the perfect companion for your busy lifestyle.",
    image: "https://example.com/smartphone_image.jpg"
  },
  {
    title: "Headphones",
    description: "Immerse yourself in crisp audio and immersive soundscapes with high-quality headphones. Whether you're jamming to your favorite tunes, gaming with friends, or tuning into podcasts, enjoy superior sound quality and comfort for extended listening sessions.",
    image: "https://example.com/headphones_image.jpg"
  },
  {
    title: "External Hard Drive",
    description: "Safeguard your precious files and expand your storage space with an external hard drive. Whether you're backing up important documents, storing multimedia files, or transferring data between devices, ensure peace of mind with reliable storage solutions.",
    image: "https://example.com/external_hard_drive_image.jpg"
  },
  {
    title: "Wireless Router",
    description: "Stay connected to high-speed internet and enjoy seamless connectivity with a reliable wireless router. Whether you're streaming HD videos, gaming online, or video conferencing with colleagues, optimize your network performance for smooth and uninterrupted connectivity.",
    image: "https://example.com/wireless_router_image.jpg"
  },
  {
    title: "Smartwatch",
    description: "Stay organized, motivated, and connected with a feature-packed smartwatch. From tracking fitness goals to receiving notifications on the go, enhance your daily routine with advanced health monitoring and convenient smart features.",
    image: "https://example.com/smartwatch_image.jpg"
  },
  {
    title: "Printer",
    description: "Transform digital documents into tangible copies with a reliable printer. Whether you're printing photos, documents, or creative projects, enjoy crisp and vibrant prints from the comfort of your home or office.",
    image: "https://example.com/printer_image.jpg"
  },
  {
    title: "Bluetooth Speaker",
    description: "Experience rich, immersive sound wherever you go with a portable Bluetooth speaker. Whether you're hosting outdoor gatherings, enjoying picnics, or simply relaxing at home, elevate your audio experience with wireless convenience and powerful sound performance.",
    image: "https://example.com/bluetooth_speaker_image.jpg"
  },
  {
    title: "Gaming Keyboard",
    description: "Dominate the virtual battlefield and enhance your gaming experience with a high-performance gaming keyboard. Featuring customizable RGB lighting, tactile switches, and ergonomic design, unleash your full gaming potential and enjoy precision control with every keystroke.",
    image: "https://example.com/gaming_keyboard_image.jpg"
  }
];
</script>

<template>
<section>
  <Card :products="products" />
</section>
</template>

<style lang="scss" scoped>
section {
  display: grid;
  grid-template-columns: repeat(4,1fr);
}
</style>