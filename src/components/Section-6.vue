<template>
  <div class="section6">
    <h1>Our team</h1>
    <h2>homeless packs, volunteers, guardians, overstayers, shelters and other organisations</h2>
    <div class="container">
      <div class="card">
        <img src="../assets/images/Oleksiky.jpg" alt="" />
        <h3>Oleksiky Tritenko</h3>
        <p>theater and film actor</p>
      </div>
      <div class="card">
        <img src="../assets/images/Stanislav.jpg" alt="" />
        <h3>Stanislav Boklan</h3>
        <p>Peoples's Artist of Ukraine</p>
      </div>
      <div class="card">
        <img src="../assets/images/Alexander.jpg" alt="" />
        <h3>Alexander Rudinsky</h3>
        <p>theater and film actor</p>
      </div>
      <div class="card">
        <img src="../assets/images/Oksana.jpg" alt="" />
        <h3>Oksana Zhdanova</h3>
        <p>theater and film actress</p>
      </div>
      <div class="card">
        <img src="../assets/images/Natalka.jpg" alt="" />
        <h3>Natalka Denisenko</h3>
        <p>theater and film actress</p>
      </div>
      <div class="card">
        <img src="../assets/images/Maksym.jpg" alt="" />
        <h3>Maksym Samchyk</h3>
        <p>theater and film actor</p>
      </div>
      <div class="card">
        <img src="../assets/images/Katerna.jpg" alt="" />
        <h3>Katerna Vyshneva</h3>
        <p>theater and film actress</p>
      </div>
      <div class="card">
        <img src="../assets/images/Irma.jpg" alt="" />
        <h3>Irma Vitovska</h3>
        <p>Honored Actress of Ukraine</p>
      </div>
      <div class="card">
        <img src="../assets/images/Igor.jpg" alt="" />
        <h3>Igor Potyanko</h3>
        <p>actor of theatre and cinema</p>
      </div>
      <div class="card">
        <img src="../assets/images/Dymitro.jpg" alt="" />
        <h3>Dymitro Surzhikov</h3>
        <p>Honored Artist of Ukraine</p>
      </div>
      <div class="card">
        <img src="../assets/images/Daria.jpg" alt="" />
        <h3>Daria Barihashvii</h3>
        <p>theater and film actress</p>
      </div>
      <div class="card">
        <img src="../assets/images/Vera.jpg" alt="" />
        <h3>Vera Kobzar</h3>
        <p>theater and film actress</p>
      </div>
      <div class="card">
        <img src="../assets/images/Andriy.jpg" alt="" />
        <h3>Andriy Fredynchyk</h3>
        <p>theater and film actor</p>
      </div>
      <div class="card">
        <img src="../assets/images/Nesterenko.jpg" alt="" />
        <h3>Anastasia Nesterenko</h3>
        <p>theater and film actress</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section6 {
  display: flex;
  flex-direction: column;
  background-color: $secondary;
  gap: 50px;
  width: 100%;
  min-height: 100vh;
  padding: 10%;
}

.section6 h1 {
  line-height: 30px;
  @include text-6xl;
  @include font-bold;
}

.section6 h2 {
  @include text-4xl;
  @include font-regular;
}

.section6 h3 {
  @include text-2xl;
  @include font-medium;
}

.section6 p {
  @include text-lg;
  @include font-medium;
}

.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 80px 40px;
  max-width: 1200px;
}

.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  text-align: center;
  width: 100%;
  max-width: 300px;
  height: 400px;
  padding: 4%;
}

.card img {
  width: 100%;
  height: 100%; /* Set height to 100% for square shape */
  object-fit: cover; /* Change to cover for square cropping */
  filter: grayscale(100%);
}

@media (max-width: 768px) {
  .section6 {
    gap: 20px;
  }
  .section6 h1 {
    @include text-3xl; /* Adjusted for mobile */
  }

  .section6 h2 {
    @include text-xl; /* Adjusted for mobile */
  }

  .section6 h3 {
    @include text-lg; /* Adjusted for mobile */
  }

  .section6 p {
    @include text-base; /* Adjusted for mobile */
  }

  .container {
    grid-template-columns: repeat(2, 1fr);
    gap: 35px 25px;
  }

  .card {
    height: auto;
  }

  .card img {
    height: auto; /* Maintain aspect ratio */
    width: 100%; /* Ensure it fills the card */
  }
}
</style>
