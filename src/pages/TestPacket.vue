<template>
  <div class="test-page">
    <page-banner></page-banner>
    <package-box></package-box>
    <trial-steps></trial-steps>
    <package-items></package-items>
  </div>
</template>

<script>
import Banner from '@/components/Banner';
import PackageBox from '@/components/PackageBox';
import TrialSteps from '@/components/TrialSteps';
import PackageItems from '@/components/PackageItems';

export default {
  name: 'TestPage',
  components: {
    'page-banner': Banner,
    'package-box': PackageBox,
    'trial-steps': TrialSteps,
    'package-items': PackageItems,
  },
}
</script>

<style lang="scss">
</style>
