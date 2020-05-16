<template>
  <div class="about">
    <div class="short__info">
      <p>
      Jesteśmy prężnie rozwijającym się warsztatem w Katowiach.
      Głównie zajmujemy się lakiernictwem, blacharstwem,
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
  margin-top: 15%;
  padding: 30px;
  text-align: justify;
  opacity: 0;
  animation: visible .3s .5s ease-in;
  animation-fill-mode: forwards;
}

@media (min-width: 1024px) {
  .short__info {
    margin-top: 5%;
    padding: 50px;
  }
}

.resoults {
  opacity: 0;
  justify-items: center;
  margin-bottom: 20px;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 20px;
  animation: visible .5s 1s ease-in;
  animation-fill-mode: forwards;
  @media(min-width: 768px) {
    grid-template-columns: 1fr 1fr 1fr;
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
