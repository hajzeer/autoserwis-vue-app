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

export default {
  data() {
    return {
      resoults: [
        { id: 0, photo: './assets/IMG_1834.JPG' },
        { id: 1, photo: './assets/IMG_1833.JPG' },
        { id: 2, photo: './assets/IMG_1845.JPG' },
        { id: 3, photo: './assets/IMG_1846.JPG' },
        { id: 4, photo: './assets/IMG_1847.JPG' },
        { id: 5, photo: './assets/IMG_1848.JPG' },
        { id: 6, photo: './assets/IMG_1870.JPG' },
        { id: 7, photo: './assets/IMG_1869.JPG' },
        { id: 8, photo: './assets/IMG_1868.JPG' },
        { id: 9, photo: './assets/IMG_1867.JPG' },
        { id: 10, photo: './assets/IMG_1866.JPG' },
        { id: 11, photo: './assets/IMG_1865.JPG' },
        { id: 12, photo: './assets/IMG_1842.JPG' },
        { id: 13, photo: './assets/IMG_1843.JPG' },
        { id: 14, photo: './assets/IMG_1841.JPG' },
        { id: 15, photo: './assets/IMG_1810.JPG' },
        { id: 16, photo: './assets/IMG_1808.JPG' },
        { id: 17, photo: './assets/IMG_1801.JPG' },
        { id: 18, photo: './assets/IMG_1811.JPG' },
        { id: 19, photo: './assets/IMG_1812.JPG' },
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
}

@media (min-width: 1024px) {
  .short__info {
    margin-top: 5%;
    padding: 50px;
  }
}

.resoults {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap:20px;
  @media(min-width: 768px) {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
</style>
