<template>
    <div class="router__nav">
        <div class="nav__outer">
            <div class="nav__inner">
                <router-link
                    class="path"
                    to="/"
                >
                    HOME
                </router-link>
                <router-link
                    class="path"
                    to="/about"
                >
                    O NAS
                </router-link>
                <router-link
                    class="path"
                    to="/contact"
                >
                    KONTAKT
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'RouterNav',
};
</script>

<style lang="scss">

    .router__nav {
        z-index: -1;
        width: 100%;
        height: 100vh;
        position: absolute;
        background-size: cover;
        background-repeat: no-repeat;
        padding: 0;
        top: 0;
        right: 0;
        background: rgba(245,245,245, .8);
    }

    .nav__inner {
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
  }

  .path {
      margin-bottom: 25px;
      cursor: pointer;
      border: none;
      color: black;
      font-family: Arial, Helvetica, sans-serif;
      font-size: 40px;
      text-decoration-line: none;
  }
</style>
