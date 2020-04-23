<template>
  <div class="contact">
    <HeroImageContact />
  <ul>
    <li>Autoserwis Daniel Filocha</li>
    <li>ul. Gliwicka 234 budynek 4 Katowice</li>
    <li>505 063 892</li>
    <li>autoserwis234@wp.pl</li>
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

ul {
  width: 300px;
  color: whitesmoke;
  font-family: 'Fira Sans', sans-serif;
  padding: 0;
  font-size: 1em;
  letter-spacing: .5px;
  list-style-type: none;
  margin: 0;
  padding: 0;

  li {
    margin-bottom: 10px;
  }
}

</style>
