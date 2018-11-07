<template>
  <section class="container">
    <banner></banner>
    <scenes></scenes>
  </section>
</template>

<script>
import Banner from '@/components/index/Banner.vue';
import Scenes from '@/components/index/Scenes.vue';

export default {
  components: {
    Banner,
    Scenes
  }
}
</script>

<style lang="scss">
.container {
    background: #F4F4F4;
}

</style>
