<template>
    <div class="hero__imageOuter">
        <div class="hero__image"></div>
    </div>
</template>

<script>
export default {
  name: 'HeroImage',
};
</script>

<style lang="scss" scoped>

    .hero__image {
        position: fixed;
        z-index: -2;
        width: 100%;
        height: 100vh;
        top: 0;
        left: 0;
        padding: 0;
        margin: 0;
        background-image: url('../../assets/HeroImage1.jpg');
        background-repeat: no-repeat;
        background-size:cover;
        background-position: 50% 0%;

        &::after {
            content: '';
            background: rgba(0, 0, 0, .2);
            position: absolute;
            top: 0;
            left: 0;
            z-index: 1;
            width: 100%;
            height: 100vh;
        }
    }

    @media(min-width: 1024px) {
        .hero__image {
            background-position: 50% 50%;
        }
    }
</style>
