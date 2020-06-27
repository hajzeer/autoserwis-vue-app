<template>
  <div class="about">
    <div class="short__info">
      <p>
      Jesteśmy prężnie rozwijającym się warsztatem w Katowiach.
      Zajmujemy się głównie lakiernictwem, blacharstwem,
      wymianą szyb, naprawą zderzaków oraz naprawą i konserwacją
      podwozi.
      Każdego dnia z pełną dokładnością staramy się sprostać
      wymaganiom naszych klientów. Poniżej przedstawiamy
      kilka z naszych prac
      </p>
    </div>
    <div class="resoults">
      <Items
          v-for="item in resoults"
          :item="item"
          :key="item.id"
        />
    </div>
    <div v-scrollanimation class="contact">
      <router-link
        class="path"
        to="/contact"
      >
        KONTAKT
      </router-link>
    </div>
  </div>
</template>

<script>
import Items from '@/components/AboutComponents/Items.vue';

import photo0 from '../assets/IMG_1834.png';
import photo1 from '../assets/IMG_1833.png';
import photo2 from '../assets/IMG_1845.png';
import photo3 from '../assets/IMG_1846.png';
import photo4 from '../assets/IMG_1847.png';
import photo5 from '../assets/IMG_1848.png';
import photo6 from '../assets/IMG_1870.png';
import photo7 from '../assets/IMG_1869.png';
import photo8 from '../assets/IMG_1868.png';
import photo9 from '../assets/IMG_1867.png';
import photo10 from '../assets/IMG_1866.png';
import photo11 from '../assets/IMG_1865.png';
import photo12 from '../assets/IMG_1842.png';
import photo13 from '../assets/IMG_1843.png';
import photo14 from '../assets/IMG_1841.png';
import photo15 from '../assets/IMG_1810.png';
import photo16 from '../assets/IMG_1808.png';
import photo17 from '../assets/IMG_1801.png';
import photo18 from '../assets/IMG_1811.png';
import photo19 from '../assets/IMG_1812.png';
import photo20 from '../assets/IMG_2217.png';
import photo21 from '../assets/IMG_2218.png';
import photo22 from '../assets/IMG_2219.png';
import photo23 from '../assets/IMG_2220.png';
import photo24 from '../assets/IMG_2221.png';
import photo25 from '../assets/IMG_2222.png';
import photo26 from '../assets/IMG_2223.png';
import photo27 from '../assets/IMG_2224.png';
import photo28 from '../assets/IMG_2225.png';
import photo29 from '../assets/IMG_2226.png';
import photo30 from '../assets/IMG_2227.png';
import photo31 from '../assets/IMG_2228.png';
import photo32 from '../assets/IMG_2229.png';
import photo33 from '../assets/IMG_2230.png';
import photo34 from '../assets/IMG_2231.png';
import photo35 from '../assets/IMG_2232.png';
import photo36 from '../assets/IMG_2233.png';
import photo37 from '../assets/IMG_2234.png';
import photo38 from '../assets/IMG_2235.png';
import photo39 from '../assets/IMG_2236.png';
import photo40 from '../assets/IMG_2237.png';
import photo41 from '../assets/IMG_2238.png';
import photo42 from '../assets/IMG_2239.png';
import photo43 from '../assets/IMG_2240.png';
import photo44 from '../assets/IMG_2241.png';
import photo45 from '../assets/IMG_2242.png';

export default {
  data() {
    return {
      resoults: [
        { id: 0, photo: photo0 },
        { id: 1, photo: photo1 },
        { id: 2, photo: photo2 },
        { id: 3, photo: photo3 },
        { id: 4, photo: photo4 },
        { id: 5, photo: photo5 },
        { id: 6, photo: photo6 },
        { id: 7, photo: photo7 },
        { id: 8, photo: photo8 },
        { id: 9, photo: photo9 },
        { id: 10, photo: photo10 },
        { id: 11, photo: photo11 },
        { id: 12, photo: photo12 },
        { id: 13, photo: photo13 },
        { id: 14, photo: photo14 },
        { id: 15, photo: photo15 },
        { id: 16, photo: photo16 },
        { id: 17, photo: photo17 },
        { id: 18, photo: photo18 },
        { id: 19, photo: photo19 },
        { id: 20, photo: photo20 },
        { id: 21, photo: photo21 },
        { id: 22, photo: photo22 },
        { id: 23, photo: photo23 },
        { id: 24, photo: photo24 },
        { id: 25, photo: photo25 },
        { id: 26, photo: photo26 },
        { id: 27, photo: photo27 },
        { id: 28, photo: photo28 },
        { id: 29, photo: photo29 },
        { id: 30, photo: photo30 },
        { id: 31, photo: photo31 },
        { id: 32, photo: photo32 },
        { id: 33, photo: photo33 },
        { id: 34, photo: photo34 },
        { id: 35, photo: photo35 },
        { id: 36, photo: photo36 },
        { id: 37, photo: photo37 },
        { id: 38, photo: photo38 },
        { id: 39, photo: photo39 },
        { id: 40, photo: photo40 },
        { id: 41, photo: photo41 },
        { id: 42, photo: photo42 },
        { id: 43, photo: photo43 },
        { id: 44, photo: photo44 },
        { id: 45, photo: photo45 },
      ],
    };
  },
  components: {
    Items,
  },
};
</script>

<style lang="scss" scoped>

.short__info {
  padding: 20px;
  margin-top: 15%;
  font-size: 18px;
  font-family: 'Fira Sans', sans-serif;
  opacity: 0;
  animation: visible .3s .5s ease-in;
  animation-fill-mode: forwards;
}

.before-enter {
  opacity: 0;
  transition: all .4s .4s ease-in;
}
.enter{
  opacity: 1;
}

@media (min-width: 1024px) {
  .short__info {
    margin-top: 5%;
    padding: 50px;
  }
}

.resoults {
  margin-top: 1em; ;
  opacity: 0;
  justify-items: center;
  margin-bottom: 20px;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 15px;
  animation: visible .5s 1s ease-in;
  animation-fill-mode: forwards;
  @media(min-width: 768px) {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

.contact {
  opacity: 0;
  padding: 30px;
  text-align: center;
  animation: visible .5s 1.5s ease-in;
  animation-fill-mode: forwards;
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
