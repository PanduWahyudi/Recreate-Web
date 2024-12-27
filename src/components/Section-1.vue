<script>
import { ref, onMounted, onUnmounted } from 'vue'
import { gsap } from 'gsap'
import DogCleanIcon from './icons/Dog-Clean.vue'
import CatCleanIcon from './icons/Cat-Clean.vue'
import YoutubeIcon from './icons/YoutubeIcon.vue'
import InstagramIcon from './icons/InstaGram.vue'
import FacebookIcon from './icons/FaceBook.vue'
import PatreonIcon from './icons/Patreon.vue'
import TelegramIcon from './icons/Telegram.vue'
import DownArrowIcon from './icons/Down-Arrow.vue'

export default {
  components: {
    DogCleanIcon,
    CatCleanIcon,
    InstagramIcon,
    YoutubeIcon,
    FacebookIcon,
    PatreonIcon,
    TelegramIcon,
    DownArrowIcon,
  },
  setup() {
    const currentIcon = ref(0)
    const icons = [DogCleanIcon, CatCleanIcon]
    let intervalId = null

    onMounted(() => {
      intervalId = setInterval(() => {
        const logoEl = document.querySelector('.wrapped-logo')

        // Animasi keluar
        gsap.to(logoEl, {
          y: 70, // Meningkatkan jarak bayangan ke bawah
          opacity: 0,
          duration: 0.3, // Mengurangi durasi untuk transisi lebih cepat
          onComplete: () => {
            // Ganti ikon
            currentIcon.value = (currentIcon.value + 1) % icons.length

            // Animasi masuk
            gsap.fromTo(
              logoEl,
              { y: -70, opacity: 0 }, // Meningkatkan jarak bayangan ke atas
              {
                y: 0,
                opacity: 1,
                duration: 0.3, // Mengurangi durasi untuk transisi lebih cepat
              },
            )
          },
        })
      }, 3000)
    })

    onUnmounted(() => {
      if (intervalId) {
        clearInterval(intervalId)
      }
    })

    return {
      currentIcon,
      icons,
    }
  },
}
</script>

<template>
  <div class="section1">
    <div class="wrapped">
      <div class="wrapped-title">
        <div class="wrapped-logo">
          <component :is="icons[currentIcon]" />
        </div>
        <h4>Innovative Solutions for Animals</h4>
      </div>
      <div class="wrapped-description">
        <p>charity organization</p>
        <div class="wrapped-sosmed">
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
    </div>
    <div class="wrapped2-container">
      <!-- <div class="wrapped2">
        <DownArrowIcon />
      </div> -->
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section1 {
  background-color: $warning;
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100%;
}

.wrapped {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex-grow: 1;
  gap: $spacing-lg;
}

.wrapped-logo {
  width: 500px;
}

.wrapped-title {
  @include text-6xl;
  width: 570px;
  // background-color: $secondary;
  display: flex;
  align-items: center;
  gap: $spacing-3xl;
  line-height: 1.1;
}

.wrapped-description {
  @include text-4xl;
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: $spacing-sm;
}
.wrapped-sosmed {
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
    transform: scale(0.7); // Mengubah ukuran menjadi 1.5x saat hover
  }
}

.wrapped2-container {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding-bottom: $spacing-lg;
}

.wrapped2 {
  @include text-2xl;
  width: 100px;
  height:100px;
  background-color: $secondary;
  padding: $spacing-md;
  text-align: center;
}

// Media query untuk layar mobile
@media (max-width: 768px) {
  .wrapped-title{
    width:300px;
    @include text-2xl;
  }

  .wrapped-logo{
    max-width:130px;
  }

  .wrapped-description{
    @include text-xl;
  }

  .sosmed-link{
    width: 35px;
    height:35px;
  }
}


</style>


