<template>
    <ul class="top-m-nav">
        <li class="nav-item">
            <nuxt-link to="/my">我的美团</nuxt-link>
            <ul class="sub-nav">
                <li>
                    <nuxt-link to="/">我的订单</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/">我的收藏</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/">抵用券</nuxt-link>
                </li>
            </ul>
        </li>
        <li class="nav-item mobile-app">
            <nuxt-link to="/app">手机APP</nuxt-link>
        </li>
        <li class="nav-item">
            <nuxt-link to="/center">商家中心</nuxt-link>
            <ul class="sub-nav center">
                <li>
                    <nuxt-link to="/my">登录商家中心</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/">美团智能收银</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/">我想合作</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/">手机免费开店</nuxt-link>
                </li>
            </ul>
        </li>
        <li class="nav-item">
            <nuxt-link to="/site">网站导航</nuxt-link>
            <div class="sub-nav site">
                <el-row :gutter="20">
                    <el-col :span="7">
                        <div class="grid-content bg-purple">
                            <span class="title">酒店旅游</span>
                            <ul class="hotel">
                                <li>
                                    <nuxt-link to="/hotel">国际机票</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">火车票</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">榛果民宿</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">经济型酒店</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">主题酒店</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">商务酒店</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">公寓</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">豪华酒店</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">客栈</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">青年旅社</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">度假酒店</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">别墅</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">农家院</nuxt-link>
                                </li>
                            </ul>
                        </div>
                    </el-col>
                    <el-col :span="4">
                        <div class="grid-content bg-purple">
                            <span class="title">吃美食</span>
                            <ul class="foods">
                                <li>
                                    <nuxt-link to="/hotel">烤鱼</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">特色小吃</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">烧烤</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">自助餐</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">火锅</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">代金券</nuxt-link>
                                </li>
                            </ul>
                        </div>
                    </el-col>
                    <el-col :span="4">
                        <div class="grid-content bg-purple">
                            <span class="title">看电影</span>
                            <ul class="movie">
                                <li>
                                    <nuxt-link to="/hotel">热映电影</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">热门影院</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">热映电影口碑榜</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">最受期待电影</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">国内票房榜</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">北美票房榜</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">电影排行榜</nuxt-link>
                                </li>
                            </ul>
                        </div>
                    </el-col>
                    <el-col :span="9">
                        <div class="grid-content bg-purple">
                            <span class="title">手机应用</span>
                            <ul class="app">
                                <li>
                                    <nuxt-link to="/hotel">
                                        <img
                                            src="http://s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                                        >
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">
                                        <img
                                            src="http://s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/waimai.png"
                                        >
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">
                                        <img
                                            src="http://s0.meituan.net/bs/fe-web-meituan/404d350/img/appicons/zhenguo.png"
                                        >
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">
                                        <img
                                            src="http://s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/dianping.png"
                                        >
                                    </nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/hotel">
                                        <img
                                            src="http://s1.meituan.net/bs/fe-web-meituan/404d350/img/appicons/maoyan.png"
                                        >
                                    </nuxt-link>
                                </li>
                            </ul>
                        </div>
                    </el-col>
                </el-row>
            </div>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
$basicColor: #31bbac;

.top-m-nav {
  font-size: 12px;

  .nav-item {
    position: relative;
    float: left;
    padding: 12px;

    a {
      color: #999;

      &:hover {
        color: $basicColor;
      }
    }

    .sub-nav {
      position: absolute;
      top: 40px;
      left: 0px;
      display: none;
      box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
      box-sizing: border-box;
      z-index: 10;

      li {
        padding: 12px;
        background: #fff;
        word-wrap: none;
      }

      &.center {
        left: -24px;
      }

      &.site {
        left: -1118px;
        width: 1190px;
        background: #fff;
        text-align: center;

        & .grid-content.bg-purple {
          padding: 30px;
        }

        & .title {
          color: $basicColor;
          font-size: 16px;
        }

        & .hotel,
        & .foods {
          display: grid;
          text-align: left;
          padding: 20px 30px;
        }

        & .hotel {
          padding: 20px 30px;
          grid-template-columns: 90px 90px 90px;
          grid-template-rows: 30px 30px 30px 30px;
        }

        & .foods {
          padding: 20px 0;
          grid-template-columns: 70px 80px;
          grid-template-rows: 30px 30px 30px;
        }

        & .movie {
          padding: 20px 0;
          display: block;

          li {
            padding: 9px;
          }
        }

        & .app {
            padding: 20px 0px;
            display: flex;
            justify-content: center;

            img {
                width: 60px;
                height: 60px;
            }

            li {
                padding: 0;
                margin: 5px;
            }
        }
      }
    }

    &:hover {
      background: #fff;
      box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
      box-sizing: border-box;

      .sub-nav {
        display: block;
      }
    }

    &.mobile-app {
        box-shadow: none;
        background: none;
    }
  }
}
</style>
