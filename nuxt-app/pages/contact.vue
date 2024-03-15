<template>
  <div class="header">
    <img
      src="https://images.pexels.com/photos/16780323/pexels-photo-16780323/free-photo-of-lens-ad-a-digital-camera-on-the-table.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 1 - Camera"
    />

    <img
      src="https://images.pexels.com/photos/16735218/pexels-photo-16735218/free-photo-of-close-up-of-a-flying-dji-drone.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 2 - Drone"
    />
    <img
      src="https://images.pexels.com/photos/16888144/pexels-photo-16888144/free-photo-of-electronic-devices-on-white-background.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 3 - Tech"
    />
    <img
      src="https://images.pexels.com/photos/16447041/pexels-photo-16447041/free-photo-of-hands-on-a-laptop.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 4 - Laptop"
    />
  </div>
  <div class="header">
    <img
      src="https://images.pexels.com/photos/16723034/pexels-photo-16723034/free-photo-of-close-up-of-a-sound-mixer.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 5 - Mixer"
    />

    <img
      src="https://images.pexels.com/photos/205316/pexels-photo-205316.png?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 6 - Tech Set Up"
    />
    <img
      src="https://images.pexels.com/photos/1649771/pexels-photo-1649771.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 7 - Headphones"
    />
    <img
      class="img2"
      src="https://images.pexels.com/photos/1579240/pexels-photo-1579240.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Image 8 - Game Console"
    />
  </div>

  <div>
    <h1>Contact Us</h1>
    <div class="image-container">
      <img
        src="https://images.pexels.com/photos/1365795/pexels-photo-1365795.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
        alt="XBox Controller"
      />

      <img
        src="https://images.pexels.com/photos/7238759/pexels-photo-7238759.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
        alt="Home Office Set up"
      />

      <img
        src="https://images.pexels.com/photos/4016837/pexels-photo-4016837.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
        alt="Camera Lense"
      />
    </div>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
  margin-top: 30px;
  font-size: 50px;
}

.header {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 0px;
}

img {
  width: 100%;
  height: auto;
}

.img2 {
  width: 100%;
  height: 96.5%;
}

.image-container {
  margin-top: 30px;
  gap: 12px;
  display: flex;
}

.image-container img {
  width: calc(100% / 3);
  max-width: 90%;
  height: 90%;
}

.image-grid {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
</style>
