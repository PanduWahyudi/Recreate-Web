<template>
  <div class="section2">
    <div class="wrapped">
      <h1>We are</h1>
      <p>
        team of like-minded people, socially active companies, media personalities, volunteers who
        help low-income shelters and foster carers to support homeless animals.
      </p>
    </div>
    <div class="wrapped">
      <h1>Our primary goal</h1>
      <p>
        is to provide animals with the most necessary things - food, medicine, and urgent needs for
        the livelihood of shelters. We believe in our power and the power of conscious citizens who
        care about the environment and their health, who understand the importance of helping each
        other, especially our little friends. Growth begins with your care for your loved ones.
        Animals are one of the closest creatures to humans who remain with us throughout our lives.
        We all know the healing power of warmth, grace, and big loving eyes.
      </p>

      <div class="quote">
        <div class="quote-wall"></div>
        <div>
          <q>Animals need to have friends. Just like humans.</q>
          <p>- James Herriot, All Creatures Great and Small</p>
        </div>
      </div>
      <p>
        Who else if not we should support our younger brothers, especially in difficult times? Let's
        be friends!
      </p>
    </div>

    <div class="video-container">
      <iframe
        class="video"
        src="https://www.youtube.com/embed/5Wk1rp99B7o"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section2 {
  display: flex;
  flex-direction: column;
  gap: $spacing-lg;
  background-color: $white;
  width: 100%;
  min-height: 100vh;
  padding: 10%;

  @media (max-width: 768px) {
    padding: 5%;
  }
}

.wrapped {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.wrapped h1 {
  @include text-6xl;
  @include font-bold;

  @media (max-width: 768px) {
    @include text-3xl;
  }
}

.wrapped p {
  @include text-3xl;
  @include font-medium;

  @media (max-width: 768px) {
    @include text-lg;
  }
}

.quote {
  @include text-3xl;
  margin-left: 5%;
  display: flex;
  font-style: italic;
  align-items: center;
  gap: $spacing-md;

  @media (max-width: 768px) {
    @include text-xl;
  }
}

.quote-wall {
  background-color: $secondary;
  width: 5px;
  height: 140px;

  @media (max-width: 768px) {
    height: 100px;
  }
}

.video-container {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.video {
  width: 100%;
  max-width: 100%;
  height: 90vh;
  max-height: 600px;
  border: 5px solid black;

  @media (max-width: 768px) {
    height: 250px; // Ubah tinggi video menjadi persegi panjang pada layar mobile
    max-height: none;
  }
}
</style>
