<template>
  <div class="page">
    <p class="p">hello world</p>
    <test-view></test-view>
  </div>
</template>

<script lang="ts">
import TestView from '@/components/TestView.vue'

export default {
  name: 'HomeView',
  components: {
    TestView,
  },
}
</script>

<style lang="scss" scoped>
.word {
  color: red;
}
</style>
