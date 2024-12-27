<template>
  <div class="section7">
    <h1>Our partners</h1>
    <h2>are take care of our fund and help us with many questions</h2>
    <div class="container">
      <div class="card">
        <img src="../assets/images/logo1.jpg" alt="logo1" />
      </div>
      <div class="card">
        <img src="../assets/images/logo2.png" alt="logo2" />
      </div>
      <div class="card">
        <img src="../assets/images/logo3.png" alt="logo3" />
      </div>
      <div class="card">
        <img src="../assets/images/logo4.png" alt="logo4" />
      </div>
      <div class="card">
        <img src="../assets/images/logo5.png" alt="logo5" />
      </div>
      <div class="card">
        <img src="../assets/images/logo6.jpeg" alt="logo6" />
      </div>
      <!-- Tambahkan lebih banyak card sesuai kebutuhan -->
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section7 {
  display: flex;
  flex-direction: column;
  gap: 50px;
  width: 100%;
  min-height: 100vh;
  padding: 10%;
}

.section7 h1 {
  line-height: 30px;
  @include text-6xl;
  @include font-bold;
}
.section7 h2 {
  @include text-4xl;
  @include font-regular;
}

.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 80px 50px;
}

.card {
  filter: grayscale(100%);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.card img {
  max-width: 100%;
  height: auto;
}

/* Media query untuk tampilan mobile */
@media (max-width: 768px) {
  .section7 {
    gap: 20px;
    min-height:650px
  }
  .section7 h1 {
    @include text-3xl;
  }
  .section7 h2 {

    @include text-xl;
  }
  .container {
    grid-template-columns: repeat(2, 1fr); /* Ubah menjadi 2 kolom */
    gap: 40px 20px;
  }

  .card {
    width: 90%;
    margin: 0 auto;
  }

  .card img {
    max-width: 100%;
    height: auto;
  }
}
</style>
