<template>
  <section class="package-items">
    <div class="package-items__content container">
      <h2>Contains your test package</h2>
      <div class="row row--wrap row--align-top">
        <div class="col-6 col-sm-12 text-center item">
          <div class="row">
            <div class="col-4 item__image">
              <img :src="diapersImage" class="full-width">
            </div>
            <div class="col-8 text-left item__content">
              <h3 class="text-uppercase">10 Lillydoo Diapers</h3>
              <ul>
                <li>0% perfumes & lotions, 100% LILLYDOO protection</li>
                <li>Extra soft and with an ideal fit</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-6 col-sm-12 text-center item">
          <div v-show="currentPackage <= 3">
            <div class="row">
              <div class="col-4 item__image">
                <img :src="waterWipes" class="full-width">
              </div>
              <div class="col-8 text-left item__content">
                <h3 class="text-uppercase">15 WET WIPES WITH 99% WATER</h3>
                <ul>
                  <li>0% perfumes & PEGs, 100% biodegradable</li>
                  <li>Naturally pure, extra mild, alternative to "water & cotton"</li>
                </ul>
              </div>
            </div>
          </div>
          <div v-show="currentPackage > 3">
            <div class="row">
              <div class="col-4 item__image">
                <img :src="sensitiveWipes" class="full-width">
              </div>
              <div class="col-8 text-left item__content">
                <h3 class="text-uppercase">15 SENSITIVE WET WIPES</h3>
                <ul>
                  <li>0% perfumes & PEGs, 100% biodegradable</li>
                  <li>Extra thick and compostable cloth</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import diapersImage from '@/assets/images/lillydoo-little-blowballs-design-preview-tp.jpg';
import sensitiveWipes from '@/assets/images/sensitive-wipes-15-small.jpg';
import waterWipes from '@/assets/images/water-wipes-15-small.jpg';

export default {
  data() {
    return {
      diapersImage,
      sensitiveWipes,
      waterWipes,
    }
  },
  computed: {
    currentPackage() {
      return this.$store.currentPackage;
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/mixins";
.package-items {
  &__content {
    padding: 60px 0 80px;

    h2 {
      margin-bottom:  5rem;
    }

    .item {
      padding: 1rem;
      box-sizing: border-box;

      &__image img {
        width: 125px;
        max-width: 100%;
      }

      &__content {
        margin-left: 16px;
        ul {
          padding-left: 16px;
        }
      }

      @include tablet() {
        padding-left: 0;
        padding-right: 0;

        &__image img {
          width: 105px;
        }
      }
    }
  }
}
</style>
