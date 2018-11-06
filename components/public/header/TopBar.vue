<template>
    <div class="top-bar">
        <el-row :gutter="0">
            <el-col :span="4">
                <city></city>
            </el-col>
            <el-col :span="8">
                <user/>
            </el-col>
            <el-col :span="6" :offset="6">
                <my-nav></my-nav>
            </el-col>
        </el-row>
    </div>
</template>

<script>
import City from './city.vue';
import User from './User.vue';
import MyNav from './Nav.vue';

export default {
    components: {
        City,
        User,
        MyNav
    }
};
</script>

<style lang="scss" scoped>
.top-bar {
    background: #F4F4F4;
    height: 40px;
    width: 1190px;
    margin: 0 auto;
    z-index: 99;
}

</style>
