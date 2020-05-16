<template>
  <div class="app">
    <div class="navbar">
      <router-link to="/" class="company__name">A<span>UTO</span> S<span>ERWIS</span></router-link>
      <Hamburger @openNav="visiblity = !visiblity"/>
    </div>
    <router-view />
  </div>
</template>

<script>
import Hamburger from '@/components/Hamburger.vue';


export default {


  data() {
    return {
      visiblity: false,
    };
  },

  components: {
    Hamburger,
  },

  mounted() {
    console.log(this.visiblity);
  },
};

</script>

<style lang="scss">

  body {
    background-color: burlywood;
    margin: 0;
    padding: 0;
  }


  .company__name {
    font-family: 'Fira Sans', sans-serif;
    font-size: 20px;
    font-weight: 400;
    padding: 10px;
    margin-left: 0;
    cursor: pointer;
    border: none;
    color: black;
    text-decoration: none;
    color: whitesmoke;
    letter-spacing: 2px;

    span {
      font-size: 15px;
      letter-spacing: 2px;
      font-weight: 500;
    }
  }
  @media(min-width: 1024px) {
    .company__name {
      font-size: 30px;

      span {
        font-size: 25px;
      }
    }
  }

  .navbar {
    position: fixed;
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background: transparent;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    z-index: 99;
  }

</style>
