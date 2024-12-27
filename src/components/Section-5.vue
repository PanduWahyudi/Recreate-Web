<script>
import DogCleanIcon from './icons/Dog-Clean.vue'
import CatCleanIcon from './icons/Cat-Clean.vue'
export default {
  components: {
    DogCleanIcon,
    CatCleanIcon,
  },
}
</script>

<template>
  <div class="section5">
    <h1>Our team</h1>
    <h2>homeless packs, volunteers, guardians, overstayers, shelters and other organisations</h2>
    <div class="container">
      <div class="card">
        <img src="../assets/images/DarynaDeriv.jpg" alt="" />
        <h3>Daryna Deriv</h3>
        <p>Chairman Of the board</p>
      </div>
      <div class="card">
        <img src="../assets/images/Polina.jpg" alt="" />
        <h3>Polyna Snicarenko-KulchyTska</h3>
        <p>Curator of the Foundation</p>
      </div>
      <div class="card">
        <img src="../assets/images/Bohdan.jpg" alt="" />
        <h3>Bohdan Kulchytsky</h3>
        <p>Execetutive Manager</p>
      </div>
      <div class="card">
        <img src="../assets/images/Mikhaylo.jpg" alt="" />
        <h3>Mikhaylo Derly</h3>
        <p>Operation Manager</p>
      </div>
      <div class="card">
        <img src="../assets/images/Ksenia.jpg" alt="" />
        <h3>Ksenia Nikishina</h3>
        <p>Office Manager</p>
      </div>
      <div class="card">
        <img src="../assets/images/Anna.jpg" alt="" />
        <h3>Anna Andrychuck</h3>
        <p>SMM-manager</p>
      </div>
      <div class="card">
        <img src="../assets/images/Anastasia.jpg" alt="" />
        <h3>Anastasia Kovalchuck</h3>
        <p>Director</p>
      </div>
      <div class="card">
        <img src="../assets/images/Basil.png" alt="" />
        <h3>Basil Gloo</h3>
        <p>Web Developer</p>
      </div>
      <div class="card">
        <img src="../assets/images/Lina.jpg" alt="" />
        <h3>Lina Yakobchuck</h3>
        <p>Designer</p>
      </div>
      <div class="card">
        <img src="../assets/images/Yevcehenko.jpg" alt="" />
        <h3>Anastasia Yevchenko</h3>
        <p>Translator</p>
      </div>
      <div class="card">
        <div class="icon"><DogCleanIcon /></div>
        <h3>Office Manager</h3>
        <p>open vacancy</p>
      </div>
      <div class="card">
        <div class="icon"><CatCleanIcon /></div>
        <h3>SEO spesialit</h3>
        <p>open vacancy</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section5 {
  display: flex;
  flex-direction: column;
  gap: 40px;
  width: 100%;
  min-height: 100vh;
  padding: 10%;
}

.section5 h1 {
  line-height: 30px;
  @include text-6xl;
  @include font-bold;
}
.section5 h2 {
  @include text-4xl;
  @include font-regular;
}

.section5 h3{
  @include text-xl;
  @include font-medium;
}
.section5 p {
  @include text-lg;
  @include font-medium;
}

.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 40px;
}

.card {
  background-color: $warning;
  border: 5px solid black;
  height: 400px;
  display: flex;
  gap: 10px;
  width: 100%; /* Ubah menjadi 100% agar responsif */
  max-width: 280px; /* Tambahkan max-width untuk menjaga ukuran */
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 30px;
  flex-direction: column;
}

.card img {
  width: 100%; /* Ubah menjadi 100% agar responsif */
  height: auto; /* Ubah menjadi auto untuk menjaga rasio aspek */
  max-width: 200px; /* Tambahkan max-width untuk menjaga ukuran */
  filter: grayscale(100%);
  object-fit: cover;
}

.icon {
  width: 100%; /* Ubah menjadi 100% agar responsif */
  max-width: 220px; /* Tambahkan max-width untuk menjaga ukuran */
}

/* Media query untuk perangkat mobile */
@media (max-width: 768px) {
  .container {
    grid-template-columns: repeat(2, 1fr); /* Dua kolom di perangkat mobile */
  }

  @media (max-width: 768px) {
  .section5{
    gap : 20px;
  }
  .card{
    padding:10px;
    height: 270px;
  }
  .container {
    grid-template-columns: repeat(2, 1fr);
  }

  // Penyesuaian ukuran font untuk mobile
  .section5 h1 {
    @include text-3xl;
  }

  .section5 h2 {
    @include text-xl;
  }

  .section5 h3 {
    font-size: 15px;
  }

  .section5 p {
    @include text-sm;
  }
}
}
</style>



