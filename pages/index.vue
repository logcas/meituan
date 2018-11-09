<template>
  <section class="container">
    <banner></banner>
    <scenes></scenes>
    <my-nav></my-nav>
  </section>
</template>

<script>
import Banner from '@/components/index/Banner.vue';
import Scenes from '@/components/index/Scenes.vue';
import MyNav from '@/components/index/Nav.vue';

export default {
  components: {
    Banner,
    Scenes,
    MyNav
  }
}
</script>

<style lang="scss">
.container {
    background: #F4F4F4;
}

</style>
