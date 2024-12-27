<script>
import { gsap } from 'gsap'
import { onMounted, onUnmounted } from 'vue'

export default {
  setup() {
    let scrollListener

    onMounted(() => {
      const cards = document.querySelectorAll('.content-card > div')

      // Mengatur posisi awal kartu
      gsap.set(cards, { x: -100, opacity: 0 })

      // Fungsi untuk mengatur animasi saat scroll
      const handleScroll = () => {
        const scrollY = window.scrollY

        cards.forEach((card, index) => {
          const triggerPoint = card.offsetTop - window.innerHeight + 100 // Mengatur titik pemicu
          const isVisible = scrollY > triggerPoint

          if (isVisible) {
            // Jika kartu terlihat, animasikan masuk
            gsap.to(card, {
              x: 0,
              opacity: 1,
              duration: 0.5,
              delay: index * 0.1, // Menambahkan delay untuk efek bertahap
              ease: 'power2.out',
            })
          } else {
            // Jika kartu tidak terlihat, animasikan keluar
            gsap.to(card, {
              x: -100,
              opacity: 0,
              duration: 0.5,
              delay: index * 0.1,
              ease: 'power2.out',
            })
          }
        })
      }

      // Menambahkan event listener untuk scroll
      window.addEventListener('scroll', handleScroll)
      scrollListener = handleScroll
    })

    onUnmounted(() => {
      // Hapus event listener saat komponen di-unmount
      if (scrollListener) {
        window.removeEventListener('scroll', scrollListener)
      }
    })
  },
}
</script>

<template>
  <div class="section3">
    <div class="wrapped">
      <h1>Our projects</h1>
      <p>are very different in terms of priority, scale and complexity of implementation</p>
    </div>

    <div class="content-card">
      <div class="card1">
        <h1>Emergency Aid. War 2022</h1>
        <p>
          providing food and medicine to the shelters and animals which lost their homes and
          families due to the war
        </p>
      </div>
      <div class="card2">
        <h1>Non-commercial feed line</h1>
        <p>
          construction of industrial production base where food for shelters will be produced on a
          free basis
        </p>
      </div>
      <div class="card3">
        <h1>Education and Control</h1>
        <p>
          lectures on communication, organisation and coordination of processes, control over the
          use of aid
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.section3 {
  display: flex;
  flex-direction: column;
  gap: $spacing-lg;
  background-color: $primary;
  width: 100%;
  min-height: 100vh;
  color: $white;
  padding: 10%;

  @media (max-width: 768px) {
    padding: 5%;
  }
}

.section3 h1 {
  @include text-5xl;
  @include font-semibold;

  @media (max-width: 768px) {
    @include text-3xl;
  }
}

.section3 p {
  @include text-4xl;
  @include font-regular;

  @media (max-width: 768px) {
    @include text-xl;
  }
}

.wrapped {
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.content-card {
  display: flex;
  flex-direction: column;
  gap: $spacing-md;
}

.card1,
.card2,
.card3 {
  cursor: pointer;
  width: 100%;
  display: flex;
  flex-direction: column;
  height: 300px;
  gap: 30px;
  padding-left: 3%;
  justify-content: center;
  border: 3px solid;
  border-color: $white;

  @media (max-width: 768px) {
    height: 250px;
    gap:20px;
    padding-left: 5%;
  }
}

.card1 {
  background-color: black;
}
.card2 {
  background-color: $success;
}
.card3 {
  background-color: $secondary;
}
</style>

