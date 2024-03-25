<template>
  <h1 class="header-main">Popular Demands</h1>
  <div class="container">
    <div class="item">
      <div class="image-container">
        <img
          src="https://images.pexels.com/photos/2047905/pexels-photo-2047905.jpeg"
          alt="Laptop"
        />
      </div>
      <div class="text-container">
        <h2>Laptop</h2>
        <br />
        <p class="p1">High-Performance Laptop for Work and Play</p>
        <p p class="p2">
          <br />
          Experience the perfect blend of style and performance with our sleek
          laptop. Packed with a high-performance Intel Core processor and
          vibrant Full HD display.
        </p>
        <br />
        <NuxtLink to="/products">
          <Button>View More</Button>
        </NuxtLink>
      </div>
    </div>
    <div class="item">
      <div class="image-container">
        <img
          src="https://images.pexels.com/photos/861440/pexels-photo-861440.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
          alt="Camera"
        />
      </div>
      <div class="text-container">
        <h2>Camera</h2>
        <br />
        <p class="p1">Capture Every Moment in Stunning Detail</p>
        <br />
        <p class="p2">
          Introducing our latest camera, designed to capture every moment with
          precision and clarity. Whether you're a professional photographer or
          an avid enthusiast, this camera delivers exceptional performance and
          versatility.
        </p>
        <br />
        <NuxtLink to="/products">
          <Button>View More</Button>
        </NuxtLink>
      </div>
    </div>
  </div>
  <div class="full-width-image">
    <div class="overlay-text">
      <h1>A Crew that finds Tech for you so you don't have too!</h1>

      <NuxtLink to="/contact">
        <Button> Contact Us </Button>
      </NuxtLink>
    </div>
    <img
      src="https://images.pexels.com/photos/792345/pexels-photo-792345.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Full Image of Tech"
    />
  </div>
</template>

<style scoped>
.header-main {
  font-size: 20px;
  margin-top: 40px;
  background-color: #1c3422;
  color: white;
  padding: 20px 80px;
  display: inline-block;
  animation: moveLeftAndRight 6s linear infinite alternate;
}

h1 {
  font-size: 30px;
  justify-content: center;
  margin-bottom: 20px;
  font-family: Arial, Helvetica, sans-serif;
}

h2 {
  font-family: Arial, Helvetica, sans-serif;
}

.p2 {
  font-family: "Courier New", Courier, monospace;
}

.p1 {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}

.container {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.item {
  display: flex;
  align-items: center;
  margin: 0 20px;
}

.image-container {
  width: 300px;
  height: 300px;
  margin-right: 10px;
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.text-container {
  flex: 1;
  font-size: 16px;
}

.text-container h2 {
  font-size: 20px;
  margin-bottom: 5px;
}

.text-container p {
  font-size: 16px;
}

.full-width-image {
  position: relative;
  margin-top: 50px;
}

.full-width-image img {
  width: 100%;
  height: 115vh;
  display: block;
}

.overlay-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: white;
  width: 80%;
}

.overlay-text h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.overlay-text p {
  font-size: 18px;
}

@keyframes moveLeftAndRight {
  0% {
    transform: translateX(5);
  }
  50% {
    transform: translateX(200px);
  }
  100% {
    transform: translateX(-15px);
  }
}

@media (max-width: 900px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  .full-width-image {
    width: 100%;
  }

  .item {
    flex-direction: column;
    margin-bottom: 20px;
  }

  .image-container {
    width: 80%;
    height: 330px;
    margin-right: 0;
    margin-bottom: 10px;
  }

  .text-container {
    text-align: center;
    order: 2;
    margin-bottom: 60px;
  }
}
</style>
