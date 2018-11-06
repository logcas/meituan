<template>
    <div class="top-m-user">
        <nuxt-link to="/login" class="login">立即登录</nuxt-link>
        <nuxt-link to="/reg" class="reg">注册</nuxt-link>
    </div>
</template>

<style lang="scss" scoped>
$basicColor: #31BBAC;

.top-m-user {
    font-size: 12px;
    padding-top: 12px;

    .login {
        color: #31BBAC;
    }

    .reg {
        margin-left: 10px;
        color: #999;
    }
}

</style>
