<!-- eslint-disable vue/no-reserved-component-names -->
<script>
import Section1 from '@/components/Section-1.vue'
import Section2 from '@/components/Section-2.vue'
import Section3 from '@/components/Section-3.vue'
import Section4 from '@/components/Section-4.vue'
import Section5 from '@/components/Section-5.vue'
import Section6 from '@/components/Section-6.vue'
import Section7 from '@/components/Section-7.vue'
import ContactUs from '@/components/Contact-Us.vue'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
export default {
  components: {
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
    Section6,
    Section7,
    ContactUs,
    Header,
    Footer,
  },
}
</script>

<template>
  <Header />
  <Section1 />
  <Section2 />
  <Section3 />
  <Section4 />
  <Section5 />
  <Section6 />
  <Section7 />
  <ContactUs />
  <Footer />
</template>

<style scoped></style>
