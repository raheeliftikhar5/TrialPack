<template>
  <section class="test-steps bg-gray">
    <div class="test-steps__content container">
      <h2>How it works</h2>
      <div class="row row--wrap row--align-top">
        <div class="col-4 col-sm-12 text-center planStep">
          <img :src="trialboxIcon" class="planStep__image">
          <h3 class="planStep__header text-uppercase">Your Test Package</h3>
          <p class="planStep__content">We give you the products,<br> you take over only the postage.</p>
        </div>
        <div class="col-4 col-sm-12 text-center planStep">
          <img :src="flexibilityIcon" class="planStep__image">
          <h3 class="planStep__header text-uppercase">Your Flexibility</h3>
          <p class="planStep__content">First month box after 14 days for 49,50 € received. Or cancel before the first delivery.</p>
          <a class="planStep__link text-primary" href="#">Learn more about the <br> LILLYDOO diaper subscription here</a>
        </div>
        <div class="col-4 col-sm-12 text-center planStep">
          <img :src="subscriptionIcon" class="planStep__image">
          <h3 class="planStep__header text-uppercase">Your Monthly Box</h3>
          <p class="planStep__content">WAdapt designs or delivery intervals at any time or change the diaper size.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import flexibilityIcon from '@/assets/images/lillydoo-your-flexibility-icon.svg';
import subscriptionIcon from '@/assets/images/lillydoo-your-subscription-icon.svg';
import trialboxIcon from '@/assets/images/lillydoo-your-trialbox-icon.svg';

export default {
  data() {
    return {
      flexibilityIcon,
      subscriptionIcon,
      trialboxIcon,
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
@import "../assets/styles/mixins";
.test-steps {
  &__content {
    padding: 60px 0 80px;

    h2 {
      margin-bottom:  5rem;
    }

    .planStep {
      padding: 0 1rem;
      box-sizing: border-box;
      
      &__header {
        margin: 10px 0;
      }
      &__content {
        margin: 0;
      }
      &__link {
        margin-top: 1.5rem;
        display: block;
      }

      @include tablet() {
        padding: 0 0;
        &:not(:last-child) {
          margin-bottom: 2.5rem;
        }
      }
    }
  }
}
</style>
