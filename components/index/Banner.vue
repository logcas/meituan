<template>
    <div class="center-container">
        <el-row>
            <el-col :span="5">
                <ul class="left-menu-catagory">
                    <li
                        v-for="(item,idx) in leftMenu"
                        :key="idx"
                        @mouseover="mouseover(item.type)"
                        @mouseout="mouseout"
                    >
                        <i :class="item.icon"></i>
                        <nuxt-link to="/food">{{item.name}}</nuxt-link>
                        <i class="el-icon-arrow-right"></i>
                    </li>
                </ul>
                <div
                    class="left-menu-wrapper"
                    v-if="isShowWrapper"
                    @mouseover="mouseoverWrapper"
                    @mouseout="mouseoutWrapper"
                >
                    <div class="left-menu-detail" v-for="(item,idx) in wrapperDetail" :key="idx">
                        <div class="left-menu-detail-title">
                            <nuxt-link :to="item.link" class="title">{{ item.name }}</nuxt-link>
                            <nuxt-link :to="item.link" class="more">更多</nuxt-link>
                        </div>
                        <ul class="left-menu-detail-list">
                            <li v-for="(i,idx) in item.child" :key="idx">
                                <nuxt-link :to="i.link">{{ i.name }}</nuxt-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </el-col>
            <el-col :span="19">
                <div class="right-banner">
                    <div class="swap-banner">
                        <div class="block">
                            <el-carousel trigger="click" height="240px">
                                <el-carousel-item v-for="(item,idx) in sliderImgs" :key="idx">
                                    <nuxt-link :to="item.link">
                                        <img :src="item.img" width="550px" height="240px">
                                    </nuxt-link>
                                </el-carousel-item>
                            </el-carousel>
                        </div>
                    </div>
                    <div class="ktv">
                        <nuxt-link to="/ktv"></nuxt-link>
                    </div>
                    <div class="login">
                        <img src="http://s0.meituan.net/bs/fe-web-meituan/2d05c2b/img/avatar.jpg">
                        <p class="hello">Hi！你好</p>
                        <p><nuxt-link to="/reg" class="reg-button">注册</nuxt-link></p>
                        <p><nuxt-link to="/login" class="login-button">立即登录</nuxt-link></p>
                    </div>
                    <div class="hotel">
                        <nuxt-link to="/hotel"></nuxt-link>
                    </div>
                    <div class="music">
                        <nuxt-link to="/music"></nuxt-link>
                    </div>
                    <div class="business">
                        <nuxt-link to="/business"></nuxt-link>
                    </div>
                    <div class="download-app">
                        <img src="http://s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png">
                        <p class="name">美团APP手机版</p>
                        <p><span>1元起</span>吃喝玩乐</p>
                    </div>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  computed: {
    isShowWrapper() {
      return this.currentType !== "";
    },
    wrapperDetail() {
      return this.leftMenu.filter(item => {
        return item.type === this.currentType;
      })[0].child;
    }
  },
  data() {
    return {
      currentType: "", // left-menu 当前经过的标签
      sliderImgs: [
        {
          img:
            "http://p1.meituan.net/codeman/826a5ed09dab49af658c34624d75491861404.jpg",
          link: "/2"
        },
        {
          img:
            "http://p0.meituan.net/codeman/a97baf515235f4c5a2b1323a741e577185048.jpg",
          link: "/3"
        },
        {
          img:
            "http://p0.meituan.net/codeman/33ff80dc00f832d697f3e20fc030799560495.jpg",
          link: "/4"
        },
        {
          img:
            "http://p1.meituan.net/codeman/e419ae8488f776407459b0ee7eada070286451.jpg",
          link: "/5"
        }
      ],
      leftMenu: [
        {
          type: "food",
          name: "美食",
          icon: "el-icon-share",
          child: [
            {
              name: "美食",
              link: "/food",
              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "takeout",
          name: "外卖",
          icon: "el-icon-share",
          child: [
            {
              name: "外卖",
              link: "/food",
              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "hotel",
          name: "酒店",
          icon: "el-icon-more",
          child: [
            {
              name: "酒店",
              link: "/food",
              child: [
                { name: "酒店1", link: "/food/hotpot" },
                { name: "酒店2", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "home",
          name: "榛果民宿",
          icon: "el-icon-menu",
          child: [
            {
              name: "榛果民宿",
              link: "/food",
              child: [
                { name: "榛果民宿1", link: "/food/hotpot" },
                { name: "榛果民宿2", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "movie",
          name: "猫眼电影",
          icon: "el-icon-printer",
          child: [
            {
              name: "正在上映",
              link: "/movie",
              child: [
                { name: "变性金刚1", link: "/movie/sexking1" },
                { name: "变性金刚2", link: "/movie/sexking1" },
                { name: "变性金刚3", link: "/movie/sexking1" },
                { name: "变性金刚4", link: "/movie/sexking1" },
                { name: "变性金刚5", link: "/movie/sexking1" },
                { name: "变性金刚6", link: "/movie/sexking1" },
                { name: "变性金刚7", link: "/movie/sexking1" },
                { name: "变性金刚8", link: "/movie/sexking1" },
                { name: "变性金刚9", link: "/movie/sexking1" },
                { name: "变性金刚X", link: "/movie/sexking1" }
              ]
            },
            {
              name: "即将上映",
              link: "/movie",

              child: [
                { name: "来自屎坑的你1", link: "/movie/jackslowfuck" },
                { name: "来自屎坑的你2", link: "/movie/jackslowfuck" }
              ]
            }
          ]
        },
        {
          type: "ticket",
          name: "机票 / 火车票",
          icon: "el-icon-tickets",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "ktv",
          name: "休闲娱乐 / KTV",
          icon: "el-icon-sort",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "life",
          name: "生活服务",
          icon: "el-icon-date",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "beauty",
          name: "丽人 / 美发 / 医学美容",
          icon: "el-icon-goods",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "marrige",
          name: "结婚 / 婚纱摄影 / 婚宴",
          icon: "el-icon-time",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "child",
          name: "亲子 / 儿童乐园 / 幼教",
          icon: "el-icon-bell",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "sport",
          name: "运动健身 / 健身中心",
          icon: "el-icon-location",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "decoration",
          name: "家装 / 建材 / 家居",
          icon: "el-icon-phone",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "training",
          name: "学习培训 / 音乐培训",
          icon: "el-icon-picture",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "care",
          name: "医疗健康 / 宠物 / 爱车",
          icon: "el-icon-delete",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        },
        {
          type: "drink",
          name: "酒吧 / 密室逃脱",
          icon: "el-icon-setting",
          child: [
            {
              name: "美食",
              link: "/food",

              child: [
                { name: "火锅", link: "/food/hotpot" },
                { name: "西餐", link: "/food/westfood" }
              ]
            }
          ]
        }
      ]
    };
  },
  methods: {
    mouseover(type) {
      console.log(type);
      if (this._wrapper) {
        clearTimeout(this._wrapper);
      }
      this.currentType = type;
    },
    mouseout() {
      console.log("mouseout");
      this._wrapper = setTimeout(() => {
        this.currentType = "";
      }, 200);
    },
    mouseoverWrapper() {
      if (this._wrapper) {
        clearTimeout(this._wrapper);
      }
    },
    mouseoutWrapper() {
      console.log("mouseout");
      this._wrapper = setTimeout(() => {
        this.currentType = "";
      }, 200);
    }
  },
  mounted() {
    let arr = this.leftMenu.filter(item => {
      return item.type === "food";
    });
    console.log(arr);
  }
};
</script>

<style lang="scss" scoped>
$basicColor: #31bbac;

.center-container {
  width: 1190px;
  margin: 0 auto;
}

.left-menu-catagory {
  margin-top: 0px;
  padding-top: 10px;
  color: #fff;
  background: $basicColor;
  width: 230px;

  a {
    color: #fff;
  }

  li {
    line-height: 26px;
    position: relative;
    font-size: 5px;

    i {
      opacity: 0.5;
      margin-left: 10px;
    }

    i.el-icon-arrow-right {
      position: absolute;
      top: 50%;
      right: 10px;
      transform: translateY(-50%);
      opacity: 1;
    }

    a {
      margin-left: 10px;
      font-size: 14px;
    }

    &:hover {
      background: #399c91;
      cursor: pointer;
    }
  }
}

.left-menu-wrapper {
  width: 400px;
  height: 416px;
  position: absolute;
  top: 10px;
  left: 230px;
  background: #fff;
  color: #666;
  overflow: hidden;
  z-index: 99;
}

.left-menu-detail {
  padding: 35px;
  margin-bottom: 20px;
  .left-menu-detail-title {
    position: relative;
    padding-bottom: 10px;
    border-bottom: 1px solid #e5e5e5;
    margin-bottom: 10px;

    .more {
      position: absolute;
      top: 50%;
      right: 0;
      transform: translateY(-80%);
      font-size: 12px;
      color: #666;
    }
  }

  .left-menu-detail-list {
    li {
      float: left;
      margin-right: 13px;
      margin-bottom: 13px;
      font-size: 12px;

      a {
        color: #666;

        &:hover {
          color: $basicColor;
        }
      }
    }
  }
}

.right-banner {
  margin-top: 10px;
  margin-left: -5px;
  display: grid;
  grid-template-columns: 270px 270px 150px 230px;
  grid-template-rows: 240px 167px;
  grid-gap: 10px;

  .swap-banner {
    grid-column-start: 1;
    grid-column-end: 3;
  }

  .ktv {
    position: relative;

    background: url(http://p0.meituan.net/codeman/e473bb428f070321269b23370ff02ba956209.jpg);
    background-size: 100%;

    a {
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
  }

  .hotel {
    position: relative;
    background: url(http://p1.meituan.net/codeman/8cce56c467a17e04f3094d1e455462a0132772.png);
    background-size: 100%;

    a {
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
  }

  .music {
    position: relative;
    background: url(http://p1.meituan.net/codeman/16442c19da1f1c4544f794e29d99c92051716.jpg);
    background-size: 100%;

    a {
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
  }

  .business {
      position: relative;
      background: url(http://p1.meituan.net/codeman/5b21cddb4bb1cbc3a9c3bce0f726c75940469.jpg);
      background-size: 100%;

    a {
      display: block;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
  }

  .download-app,.login {
      text-align: center;
      background: #fff;
      border: 1px solid #e5e5e5;
      font-size: 12px;

      img {
          margin-top: 10px;
          width: 95px;
          height: 95px;
      }

      .name {
          font-size: 16px;
      }

      span {
          color: red;
      }
  }

  .login {
      img {
          margin-top: 30px;
          width: 55px;
          height: 55px;
          border-radius: 22.5px;
      }

      p.hello {
          font-size: 16px;
      }

      .login-button,.reg-button {
          display: inline-block;
          margin: 10px;
          width: 120px;
          height: 40px;
          line-height: 40px;
          font-size: 14px;
          border: 1px solid #e5e5e5;
          border-radius: 20px;

          &:hover {
              background: #f3f1f1;
              transition: 0.5s all ease-in-out;
          }
      }
  }
}
</style>
