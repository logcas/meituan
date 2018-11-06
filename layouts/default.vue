<template>
  <el-container>
  <el-header style="padding:0" height="197px">
    <my-header></my-header>
  </el-header>
  <el-main style="padding:0;">
    <nuxt/>
  </el-main>
  <el-footer style="padding:0">Footer</el-footer>
</el-container>
</template>

<script>
import MyHeader from '@/components/public/header/Index.vue';

export default {
  components: {
    MyHeader,
  }
}
</script>


<style>

</style>
