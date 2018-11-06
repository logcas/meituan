<template>
    <div class="search">
        <div class="center-container">
            <el-row :gutter="0">
                <el-col :span="5">
                    <nuxt-link to="/">
                        <img
                            src="https://s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png"
                            alt="meituan"
                            width="126px"
                            height="46px"
                        >
                    </nuxt-link>
                </el-col>
                <el-col :span="11">
                    <el-input placeholder="搜索商家或地点" v-model="search" size="large">
                        <el-button slot="append" icon="el-icon-search" class="search-button"></el-button>
                    </el-input>
                    <dl>
                        <dd>
                            <nuxt-link to="/1">热门搜索</nuxt-link>
                        </dd>
                        <dd>
                            <nuxt-link to="/1">热门搜索</nuxt-link>
                        </dd>
                        <dd>
                            <nuxt-link to="/1">热门搜索</nuxt-link>
                        </dd>
                        <dd>
                            <nuxt-link to="/1">热门搜索</nuxt-link>
                        </dd>
                        <dd>
                            <nuxt-link to="/1">热门搜索</nuxt-link>
                        </dd>
                    </dl>
                </el-col>
            </el-row>
        </div>
        <div class="center-container menu">
            <el-row>
                <el-col :span="5">
                    <div class="left-menu-catagory">
                        <span>全部分类</span>
                    </div>
                </el-col>
                <el-col :span="19">
                    <ul class="banner-top-menu">
                        <li>
                            <nuxt-link to="/takeout" class="takeout">美团外卖</nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/movie" class="movie">猫眼电影</nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/hotel" class="hotel">美团酒店</nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/hotel" class="home">民宿／公寓</nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/business" class="business">商家入驻</nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/love" class="love">美团公益</nuxt-link>
                        </li>
                    </ul>
                </el-col>
            </el-row>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            search:'',
        }
    }
};
</script>

<style lang="scss" scoped>
$basicColor: #31bbac;

.search {
  background: #fff;
  font-size: 12px;
  color: #999;
  box-shadow: 0 5px 10px -5px rgba(0, 0, 0, 0.1);
  height: 157px;

  .center-container {
    padding-top: 28px;
  }

  dl dd a {
    float: left;
    margin-right: 10px;
    margin-top: 9px;
    color: #999;

    &:hover {
      color: $basicColor;
    }
  }
}

.center-container.menu {
    margin-top: -15px;
}

.left-menu-catagory {
    width: 230px;
    height: 50px;
    padding-top: 15px;
    background: $basicColor;
    color: #fff;
    font-size: 16px;

    span {
        margin-left: 16px;
    }
}

.banner-top-menu {
    margin-top: 15px;
    margin-left: 20px;

    li {
        float: left;
        margin: 0 20px;
        font-size: 16px;
        font-weight: bold;

        a:hover.takeout,a:hover.home {
            color: orange;
        }

        a:hover.hotel,a:hover.movie,a:hover.love {
            color: red;
        }

        a:hover.business {
            color: $basicColor;
        }
    }
}
</style>
