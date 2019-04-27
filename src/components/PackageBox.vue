<template>
  <section class="test-package">
    <div class="test-package__content container">
      <div class="row row--wrap row--space-between packages">
        <div class="col-6 col-sm-12 packages__image">
          <img :src="testPacket10" class="full-width" v-show="currentPackage === 1">
          <img :src="testPacket20" class="full-width" v-show="currentPackage === 2">
          <img :src="testPacket30" class="full-width" v-show="currentPackage === 3">
          <img :src="testPacket40" class="full-width" v-show="currentPackage === 4">
          <img :src="testPacket50" class="full-width" v-show="currentPackage === 5">
        </div>
        <div class="col-5 col-sm-12 text-left packages__list">
          <h2>Our free test package</h2>
          <p class="text-uppercase">Choose Your Size</p>
          <div class="row">
            <div class="col col-sm-4 text-center option" :class="{'selected': currentPackage === 1}" @click="setCurrentPackage(1)">
              <span class="option__header">1</span>
              <span class="option__subheader">(2-3KG)</span>
            </div>
            <div class="col col-sm-4 text-center option" :class="{'selected': currentPackage === 2}" @click="setCurrentPackage(2)">
              <span class="option__header">2</span>
              <span class="option__subheader">(3-4KG)</span>
            </div>
            <div class="col col-sm-4 text-center option" :class="{'selected': currentPackage === 3}" @click="setCurrentPackage(3)">
              <span class="option__header">3</span>
              <span class="option__subheader">(4-7KG)</span>
            </div>
            <div class="col col-sm-4 text-center option" :class="{'selected': currentPackage === 4}" @click="setCurrentPackage(4)">
              <span class="option__header">4</span>
              <span class="option__subheader">(7-10KG)</span>
            </div>
            <div class="col col-sm-4 text-center option" :class="{'selected': currentPackage === 5}" @click="setCurrentPackage(5)">
              <span class="option__header">5</span>
              <span class="option__subheader">(10-12KG)</span>
            </div>
          </div>
          <p>Test our diapers and wipes now - In size 1 - 3 our test package contains our wipes with 99% water, from Gr. 4 you will receive our Sensitive Wet Wipes. We pay the products, you only the shipping.</p>
          <ul>
            <li class="text-primary">Automatic transition to the ever-terminable diaper subscription for € 49.50 per delivery.</li>
            <li>Prices include VAT, plus <a class="text-primary" href="#">shipping costs</a></li>
          </ul>
          <button class="button button--fw">ADD TO CART</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import testPacket10 from '@/assets/images/lillydoo-testpaket-10.jpg';
import testPacket20 from '@/assets/images/lillydoo-testpaket-20.jpg';
import testPacket30 from '@/assets/images/lillydoo-testpaket-30.jpg';
import testPacket40 from '@/assets/images/lillydoo-testpaket-40.jpg';
import testPacket50 from '@/assets/images/lillydoo-testpaket-50.jpg';
import standardBadge from '@/assets/images/oekotex_de.png';

export default {
  data() {
    return {
      testPacket10,
      testPacket20,
      testPacket30,
      testPacket40,
      testPacket50,
      standardBadge,
    }
  },
  computed: {
    currentPackage() {
      return this.$store.currentPackage;
    }
  },
  methods: {
    setCurrentPackage(pack) {
      this.$store.currentPackage = pack;
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
@import "../assets/styles/mixins";
.test-package {
  &__content {
    padding: 40px 0;

    .packages {
      &__image {
        padding: 0 20px;
        box-sizing: border-box;
      }

      &__list {
        min-width: 345px;
        ul {
          padding-left: 16px;
          margin: 15px 0 2.5rem;
        }

        .option {
          margin-right: 0.9rem;
          border: 1px solid $gray;
          color: $gray;
          padding: 4px 10px;
          box-sizing: border-box;
          cursor: pointer;

          &:last-child {
            margin-right: 0;
          }

          &:hover, &.selected {
            background: $primary;
            border: 1px solid $primary;
            color: $white;
          }

          &__header {
            width: 100%;
            display: block;
            font-size: 1.2rem;
            font-weight: bold;
          }

          &__subheader {
            width: 100%;
            display: block;
            font-size: 0.85rem;
          }
        }
        
        @include tablet() {
          margin-top: 2rem;
          min-width: unset;
        }

        @include mobileL() {
          .row {
            justify-content: flex-start;
            flex-wrap: wrap;

            .option {
              width:  27%;
              margin-bottom: 1rem;
            }
          }
        }
      }
    }
  }
}
</style>
