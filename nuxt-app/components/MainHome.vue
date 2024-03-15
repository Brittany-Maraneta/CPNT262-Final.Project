<template>
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
        <p>Description goes here for item 1.</p>
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
        <p>Description goes here for item 2.</p>
      </div>
    </div>
  </div>
  <div class="full-width-image">
    <div class="overlay-text">
      <h1>A Crew that finds Tech for you so you don't have too!</h1>
      <Button>
        Contact Us
      </Button>
    </div>
    <img
      src="https://images.pexels.com/photos/792345/pexels-photo-792345.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
      alt="Full Image of Tech"
    />
  </div>
</template>

<style scoped>
h1 {
  font-size: 30px;
  justify-content: center;
  margin-bottom: 20px;
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


@media (max-width: 768px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  .full-width-image {
    width: 100%;
  }

  .item {
    margin-bottom: 20px;
  }

  .image-container {
    width: 80%;
    height: 70%;
  }

  .text-container {
    text-align: center;
  }
}
</style>
