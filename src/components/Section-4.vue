<script>

export default {
  data() {
    return {
      dummyData: [
        'Shelter of Victoria',
        'City of faithul hearts',
        'Shelter Of Natalia Tymoshenko',
        'Shelter of Jeanne Sass',
        'Shelter Of Victoria Bondarenko',
        'Sterilization center',
        'Zoo chance',
        'Save lives',
        'City Center for the Treatment of Animals',
        'Society for the Protection of Animals in Sumy',
        'The right to life',
        '4 paws',
        'The kingdom of cats',
        'Zvir',
        'Mercy',
        'Happy dog',
        'Give me a paw, friend',
        'Friend',
        'Hope',
        'We are the right to life',
        'Planeta',
        'Second Life',
        'Happy Shore',
        'Retrieverteam',
        'Shelter of Irina Dobrolyubova',
        'Matilda',
        'Life',
        'Second chance',
        'SOS',
        'Best Friends',
      ],
    }
  },
}
</script>

<template>
  <div class="section4">
    <h1>We want to help</h1>
    <h2>homeless packs, volunteers, guardians, overstayers, shelters and other organisations</h2>
    <div class="content-card">
      <div class="card" v-for="(name, index) in dummyData" :key="index">
        <p>{{ name }}</p>
      </div>
    </div>
    <div class="apply">
      apply for help
      <img src="../assets/images/arrow.png" alt="arrow" class="arrow-img" />
    </div>
  </div>
</template>


<style lang="scss" scoped>
.section4 {
  display: flex;
  flex-direction: column;
  gap: $spacing-lg;
  background-color: $warning;
  width: 100%;
  min-height: 100vh;
  padding: 10%;
}

.section4 h1 {
  @include text-5xl;
  @include font-semibold;
}

.section4 h2 {
  @include text-4xl;
  @include font-regular;
}

.section4 p {
  @include text-2xl;
  @include font-regular;
}

.content-card {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.card {
  background-color: $white;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 3px solid black;
  text-align: center;
  height: 100px;
}

.apply {
  cursor: pointer;
  background-color: $secondary;
  @include text-3xl;
  @include font-semibold;
  border: 3px solid black;
  width: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  padding: 10px;
  position: relative;
  transition: all 0.3s ease;
}

.arrow-img {
  width: 70px;
  height: 30px;
  transition: transform 0.3s ease;
  transform: scaleX(-1);
}

.apply:hover .arrow-img {
  transform: translateX(20px) scaleX(-1);
}

/* Media query untuk perangkat mobile */
@media (max-width: 768px) {
  .section4 {
    gap:20px;
    padding: 5%;
  }

  .section4 h1 {
    @include text-3xl;
  }

  .section4 h2 {
    @include text-base;
  }

  .section4 p {
    @include text-base;
  }

  .content-card {
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }

  .card {
    height: 80px;
    padding: 10px;
  }

  .apply {
    width: 100%;
    max-width: 250px;
    @include text-lg;
  }

  .arrow-img {
    width: 50px;
    height: 20px;
  }
}
</style>
