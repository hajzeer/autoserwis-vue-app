<template>
  <div class="contact">
    <HeroImageContact />
  <ul class="contact__list">
    <li><router-link to="/">Autoserwis Daniel Filocha</router-link></li>
    <li>
      <a href="https://goo.gl/maps/NJXbx6hdg1g4heXy7">
        ul. Gliwicka 234 budynek 4 Katowice
        <br/>
        (Prowadź do Nas)
      </a>
    </li>
    <li>
      <a href="tel:+48-505-063-892">
        505 063 892
        <br/>
        (Zadzwoń do Nas)
      </a>
    </li>
    <li>
      <a href="mailto: autoserwis234@wp.pl">
        autoserwis234@wp.pl
        <br/>
        (Napisz do Nas)
      </a>
    </li>
  </ul>
  </div>
</template>

<script>
import HeroImageContact from '@/components/ContactComponents/HeroImageContact.vue';

export default {
  name: 'Contact',
  components: {
    HeroImageContact,

  },
};
</script>

<style lang="scss" scoped>

body {
  padding: 0;
  margin: 0;
}
.contact {
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
}

.contact__list {
  width: 400px;
  color: whitesmoke;
  font-family: 'Fira Sans', sans-serif;
  padding: 0;
  font-size: 1em;
  letter-spacing: .5px;
  list-style-type: none;
  margin: 0;
  padding: 0;

  li {
    margin-bottom: 20px;

    a {
      text-decoration: none;
      color: whitesmoke;
    }
  }
}

 @media(min-width: 768px) {
    .contact__list {
      margin-top: -20px;
        li {
          width: 100%;
          font-size: 1.5em;
          letter-spacing: 1px;
        }
      }
    }

  @media(min-width: 1024px) {
    .contact__list {
      margin-top: -20px;
      li {
        font-size: 1.5em;
        letter-spacing: 2px;
      }
    }
  }

</style>
