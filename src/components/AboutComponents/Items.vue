<template>
        <img v-scrollanimation :src="photos" class="item"/>
</template>

<script>
export default {
  name: 'Items',
  props: {
    item: {
      type: Object,
      requuired: true,
    },
  },
  data() {
    return {
      photo: this.item.photo,
    };
  },
  computed: {
    photos() {
      return `${this.photo}`;
    },
  },
};
</script>

<style lang="scss" scoped>
.before-enter {
  opacity: 0;
  transition: all .4s .4s ease-in;
}
.enter{
  opacity: 1;
}

.item {
  width: 80vw;
  height: 250px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50%;
  z-index: 1;
  box-shadow: 0 10px 15px -8px rgba(0,0,0, .8);

  @media (min-width: 768px) {
    width: 25vw;
  }
}
</style>
