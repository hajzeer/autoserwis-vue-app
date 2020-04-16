<template>
  <div class="home">
    <HeroImage />
    <div class="service">
      <p class="service__name">BLACHARSTWO</p>
      <p class="service__name">LAKIERNICTWO</p>
      <p class="service__name">WYNIANA SZYB</p>
      <p class="service__name">NAPRAWA ZDERZAKÓW</p>
      <p class="service__name">NAPRAWA I KONSETWACJA PODWOZI</p>
    </div>
  </div>
</template>

<script>
import HeroImage from '@/components/HomeComponents/HeroImage.vue';

export default {
  name: 'Home',

  components: {
    HeroImage,
  },
};
</script>

<style lang="scss" scoped>
  .home {
    width: 100%;
    z-index: -99;
  }

  .service {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 50%;

    .service__name {
      color: whitesmoke;
      font-family: 'Fira Sans', sans-serif;
      padding: 0;
      font-size: 15px;
      text-decoration-line: underline;
      letter-spacing: .5px;
    }
  }
</style>
