<template>
    <div class="header">
        <top-bar></top-bar>
        <search></search>
    </div>
</template>

<script>
import TopBar from './TopBar.vue';
import Search from './Search.vue';
export default {
    components: {
        TopBar,
        Search
    }
}
</script>

<style lang="scss" scoped>
.header {
    width: 100%;
    background: #F4F4F4;
}
</style>
