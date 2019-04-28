<template>
  <section class="banner">
    <div class="banner__content container">
      <div class="col-6 col-sm-12">
        <h1>Discover our skin friendliness</h1>
        <button class="button" @click="scrollToPackageBox">NOW CHOOSE YOUR SIZE</button>
      </div>
    </div>
  </section>
</template>

<script>
import standardBadge from '@/assets/images/oekotex_de.png';

export default {
  data() {
    return {
      standardBadge,
    }
  },
  methods: {
    scrollToPackageBox() {
      const ele = document.getElementById("package-box");
      if (ele) {
        window.scrollTo({
          top: ele.offsetTop,
          left: 0,
          behavior: 'smooth'
        });
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins";
.banner {
  display: flex;
  align-items: center;
  max-height: 550px;
  height: 37vw;
  background-size: cover;
  background-image: url('../assets/images/lillydoo-testpaket-header-large.jpg');

  @include tablet() {
    padding: 20px;
    height: 100vh;
    align-items: unset;
  }

  &__content {
    // width: 100%;
    // padding-left: 7vw;

    @include tablet() {
      padding-left: unset;
      margin-top: 5rem;

      h1 {
        margin-bottom: 5%;
      }

      .button {
        width: 80%;
      }
    }

    @include mobileL() {
      .button {
        width: 100%;
      }
    }
  }

  @include tablet() {
    background-image: url('../assets/images/lillydoo-testpaket-header-medium.jpg');
    background-position: center center;
  }

  @include mobileM() {
      background-image: url('../assets/images/lillydoo-testpaket-header-small.jpg');
  }
}
</style>
