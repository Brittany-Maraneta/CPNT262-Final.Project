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
    <h2>
      Looking to dive deeper into the world of technology? Our team of experts
      is here to assist you every step of the way. Whether you have questions
      about the latest gadgets, need help troubleshooting tech issues, or want
      to explore innovative solutions for your business, we've got you covered.
      Contact us today to unleash the power of technology and take your digital
      journey to new heights.
    </h2>
    <div class="image-container">
      <div class="image-with-text">
        <img
          src="https://images.pexels.com/photos/1365795/pexels-photo-1365795.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
          alt="XBox Controller"
        />
        <NuxtLink to="/products">
          <div class="text">View Products</div>
        </NuxtLink>
      </div>

      <div class="image-with-text">
        <img
          src="https://images.pexels.com/photos/7238759/pexels-photo-7238759.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
          alt="Home Office Set up"
        />
        <div class="text">Troubleshooting</div>
      </div>

      <div class="image-with-text">
        <img
          src="https://images.pexels.com/photos/4016837/pexels-photo-4016837.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
          alt="Camera Lense"
        />
        <div class="text">Questions</div>
      </div>
    </div>
  </div>
  
  <div class="contact-form-container">
    <div class="logo">
    <img src ="../public/logo.svg" alt="logo"></img>
  </div>
    <h2>Contact Us</h2>
    <form id="contact-form">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required />
      </div>
      <div class="form-group">
        <label for="last-name">Last Name:</label>
        <input type="text" id="last-name" name="last-name" required />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" name="message" rows="4" required></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<style scoped>
h1 {
  text-align: center;
  margin-top: 30px;
  font-size: 50px;
  margin-bottom: 30px;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

h2 {
  text-align: center;
  margin-top: 30px;
  margin-left: 160px;
  margin-right: 160px;
  font-size: 18px;
  margin-bottom: 30px;
  font-family: "Courier New", Courier, monospace;
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
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  padding: 10px;
  border-radius: 8px;
  font-size: 16px;
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
  
}

.image-with-text {
  position: relative;
  width: calc(33.33% - 10px);
  margin-bottom: 20px;
}

.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 200px; 
  height: auto; 
  background-color: lightgrey;
  border-radius: 10px;
}


@media (max-width: 768px) {
  .image-container {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  }
}

@media (max-width: 480px) {
  .image-with-text {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }

  .contact-form-container {
    max-width: 200px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
  }
}

.contact-form-container {
  max-width: 700px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

.contact-form-container h2 {
  text-align: center;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button[type="submit"] {
  width: 100%;
  padding: 10px;
  background-color: #9fcbaa;
  color: black;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button[type="submit"]:hover {
  background-color: #1c3422;
  color: white;
}
</style>
