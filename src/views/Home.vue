<template>
  <div class="home">
    <HeroImage />
    <div class="service">
                      <router-link
                    class="path"
                    to="/about"
                >
      <p class="service__name">BLACHARSTWO</p>
      <p class="service__name">LAKIERNICTWO</p>
      <p class="service__name">WYNIANA SZYB</p>
      <p class="service__name">NAPRAWA ZDERZAKÓW</p>
      <p class="service__name">NAPRAWA I KONSERWACJA PODWOZI</p>
      </router-link>
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
    text-align: center;

    .service__name {
      opacity: 0;
      width: 300px;
      color: whitesmoke;
      font-family: 'Fira Sans', sans-serif;
      padding: 0;
      font-size: 15px;
      text-decoration-line: underline;
      letter-spacing: .5px;
      animation: visible .5s .5s ease-in;
      animation-fill-mode: forwards;
    }

  }

  @media(min-width: 768px) {
    .service {
      margin-top: -20px;
        .service__name {
          width: 100%;
          font-size: 20px;
          letter-spacing: 1px;
        }
      }
    }

  @media(min-width: 1024px) {
    .service {
      margin-top: -20px;
      .service__name {
        font-size: 40px;
        letter-spacing: 2px;
      }
    }
  }
  @keyframes visible {
  from {
    opacity: 0;
  }
  to{
    opacity: 1;
  }
}
</style>
