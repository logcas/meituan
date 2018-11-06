<template>
  <el-container>
  <el-header style="padding:0" height="197px">
    <my-header></my-header>
  </el-header>
  <el-main style="padding:0;">
    <nuxt/>
  </el-main>
  <el-footer style="padding:0">
    <my-footer></my-footer>
  </el-footer>
</el-container>
</template>

<script>
import MyHeader from '@/components/public/header/Index.vue';
import MyFooter from '@/components/public/footer/Index.vue';

export default {
  components: {
    MyHeader,
    MyFooter
  }
}
</script>


<style>

</style>
