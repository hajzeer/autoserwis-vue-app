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
    height: auto;
    z-index: -99;
  }

  .service {
    width: 100%;
    height: 100vh;
    margin: 0;
    padding: 0;
    top: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: -20px;

    .service__name {
      color: whitesmoke;
      font-family: 'Fira Sans', sans-serif;
      padding: 0;
      font-size: 15px;
      text-decoration-line: underline;
      letter-spacing: .5px;
    }

  }

  @media(min-width: 768px) {
    .service {
      margin-top: -20px;
        .service__name {
          font-size: 25px;
          letter-spacing: 1px;
        }
      }
    }

  @media(min-width: 1024px) {
    .service {
      margin-top: -20px;
      .service__name {
        font-size: 35px;
        letter-spacing: 2px;
      }
    }
  }
</style>
