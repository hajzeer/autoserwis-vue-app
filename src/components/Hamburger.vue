<template>
<div>
    <button
        class="hamburger"
        :class="{active: isActive}"
        @click="$emit('openNav'), toggleClick()"
      >
        <span class="hamburger__box">
            <span class="hamburger__inner" />
        </span>
    </button>
      <transition name="slide-fade">
      <div v-if="isActive">
        <RouterNav />
      </div>
      </transition>
    </div>
</template>

<script>
import RouterNav from '@/components/RouterNav.vue';

export default {
  name: 'Hamburger',

  data() {
    return {
      isActive: false,
    };
  },
  components: {
    RouterNav,
  },

  methods: {
    toggleClick() {
      this.isActive = !this.isActive;
    },
  },
  watch: {
    $route() {
      this.isActive = false;
    },
  },
};
</script>

<style lang="scss" scoped>

.hamburger {
    padding: 10px;
    z-index: 2;
    display: inline;
    cursor: pointer;
    background-color: transparent;
    border: 0;
    margin-right: 0;
}

.hamburger__box {
    width: 35px;
    height: 24px;
    display: inline-block;
    position: relative;
}

.hamburger__inner {
    width: 100%;
    height: 3px;
    background-color: whitesmoke;
    position: absolute;
    right: 0;
    top: 50%;
    transition: background-color .1s .2s ease-in-out;

    &::before {
        content: '';
        width: 100%;
        height: 2px;
        position: absolute;
        background-color: whitesmoke;
        right: 0;
        top: -10px;
        transition: transform .2s .1s ease-in-out;
    }

    &::after {
        content: '';
        width: 100%;
        height: 2px;
        position: absolute;
        background-color: whitesmoke;
        right: 0;
        top: 10px;
        transition: transform .2s .1s ease-in-out;
    }
}
@media(min-width: 1024px) {
  .hamburger__box {
    width: 30px;
    height: 20px;
  }
  .hamburger__inner {
    height: 2px;
  }
}

.active .hamburger__inner {
  background-color: transparent;
}

.active .hamburger__inner:before {
  transform: translateY(10px) rotate(45deg);
  background-color: rosybrown;
}

.active .hamburger__inner:after {
  transform: translateY(-10px) rotate(-45deg);
  background-color: rosybrown;
}


.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .6s
}
.slide-fade-enter, .slide-fade-leave-to {
  opacity: 0;
}
</style>
