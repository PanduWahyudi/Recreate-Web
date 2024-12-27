<script>
import YoutubeIcon from './icons/YoutubeIcon.vue'
import InstagramIcon from './icons/InstaGram.vue'
import FacebookIcon from './icons/FaceBook.vue'
import PatreonIcon from './icons/Patreon.vue'
import TelegramIcon from './icons/Telegram.vue'
import ContactIcon from './icons/ContactIcon.vue'
export default {
  components: {
    InstagramIcon,
    YoutubeIcon,
    FacebookIcon,
    PatreonIcon,
    TelegramIcon,
    ContactIcon,
  },
}
</script>

<template>
  <div class="container">
    <div class="content1">
      <div class="description">
        <h1>Contact Us</h1>
        <h2>Kyiv Ukraine</h2>
        <h2 class="mail">mail@isa.co.ua</h2>
      </div>
      <div class="wrap-sosmed">
        <div class="sosmed-link">
          <YoutubeIcon />
        </div>
        <div class="sosmed-link">
          <InstagramIcon />
        </div>
        <div class="sosmed-link">
          <FacebookIcon />
        </div>
        <div class="sosmed-link">
          <PatreonIcon />
        </div>
        <div class="sosmed-link">
          <TelegramIcon />
        </div>
      </div>
    </div>

    <div class="content2">
      <ContactIcon />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  background-color: $success;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  height: 95vh;
  padding-left: 10%;
  padding-right: 10%;
}

h1 {
  line-height: 50px;
  @include text-6xl;
  @include font-bold;
}

h2 {
  line-height: 20px;
  @include text-4xl;
  @include font-regular;
}

.description {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.mail {
  cursor: pointer;
  transition: transform 0.3s ease; // Menambahkan transisi smooth
}

.mail:hover {
  transform: scale(0.9); // Mengubah ukuran saat hover
}

.content1 {
  display: flex;
  flex-direction: column;
  gap: 100px;
}

.wrap-sosmed {
  display: flex;
  align-items: center;
  gap: $spacing-sm;
}

.sosmed-link {
  cursor: pointer;
  width: 55px;
  height: 55px;
  transition: transform 0.3s ease; // Menambahkan transisi smooth

  &:hover {
    transform: scale(0.7); // Mengubah ukuran menjadi 0.7x saat hover
  }
}

.content2 {
  width: 600px; /* Ukuran default untuk desktop */
  height: auto;
}

/* Media Query untuk Responsif */
@media (max-width: 768px) {
  .container {
    display: block; /* Mengubah display menjadi block pada mobile */
    padding:5%;
  }

  .content1 {
    margin-bottom: 100px;
    gap: 50px;
  }

  .sosmed-link{
    width: 35px;
    height: 35px;
  }

  h1 {
    @include text-4xl;
  }

  h2 {
    @include text-2xl;
  }

  .content2 {
    width: 350px;
    margin: 0 auto;
  }
}
</style>
