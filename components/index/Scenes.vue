<template>
    <div class="scenes">
        <div class="center-container">
            <div class="scenes-header bigger-style">
                <span class="title">有格调</span>
                <ul class="nav">
                    <li class="nav-item" :class="{'active':currentType === item.type}" v-for="(item,idx) in items" :key="idx" @mouseover="mouseOver(item.type)">{{ item.name }}</li>
                </ul>
            </div>
            <div class="scenes-body clearfix">
                <nuxt-link to="/" class="card" v-for="(item,idx) in currentChild" :key="idx">
                    <div class="card-img">
                        <img
                            :src="item.img"
                            alt="meituan"
                        >
                    </div>
                    <div class="card-info">
                        <div class="title">{{ item.name }}</div>
                        <ul class="tags">
                            <li class="tag" v-for="tag in item.tags" :key="tag">{{ tag }}</li>
                        </ul>
                        <div class="price">{{ item.price }}</div>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  computed: {
    currentChild() {
      return this.items.filter(el => {
        return el.type === this.currentType;
      })[0].child;
    }
  },
  data() {
    return {
      currentType: "all",
      items: [
        {
          type: "all",
          name: "全部",
          child: [
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            }
          ]
        },
        {
          type: "meeting",
          name: "约会聚餐",
          child: [
            {
              img:
                "http://p0.meituan.net/msmerchant/8b52f948d34c5686b5c64b2bfc90b2db1198458.jpg@368w_208h_1e_1c",
              name: "必胜客",
              tags: ["大品牌", "双十一特惠"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "肯德基",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/mogu/b2cea65fd1c042975a33e3fff947a94a106864.jpg@368w_208h_1e_1c",
              name: "路边火锅",
              tags: ["双十一特惠", "国庆特惠", "重庆美食"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            }
          ]
        },
        {
          type: "spa",
          name: "丽人SPA",
          child: [
            {
              img:
                "http://p1.meituan.net/wedding/88201a40d5c40749aaf571b4ce286946164971.jpg@240w_180h_1e_1c_1l%7Cwatermark=1&&r=2&p=9&x=2&y=2&relative=1&o=20%7C368w_208h_1e_1c",
              name: "丽人SPA",
              tags: ["大品牌", "双十一特惠"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "肯德基",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/mogu/b2cea65fd1c042975a33e3fff947a94a106864.jpg@368w_208h_1e_1c",
              name: "路边火锅",
              tags: ["双十一特惠", "国庆特惠", "重庆美食"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            },
            {
              img:
                "http://p1.meituan.net/tdchotel/240f2a9555e792edf822dcf50c2d99a0239855.jpg@368w_208h_1e_1c",
              name: "中国大酒店",
              tags: ["酒店套餐", "双十一特惠", "国庆特惠", "亲子推荐"],
              price: "￥999/位"
            }
          ]
        }
      ]
    };
  },
  methods: {
      mouseOver(type) {
          this.currentType = type;
      }
  }
};
</script>

<style lang="scss" scoped>
.clearfix {
    *zoom: 1;

    &::after {
        display: block;
        content: " ";
        visibility: hidden;
        clear: both;
        height: 0;
    }
}

.scenes {
  width: 100%;
  background: #f4f4f4;
}

.center-container {
  margin: 0 auto;
  margin-top: 40px;
  width: 1190px;
}

.scenes-header {
  height: 44px;
  line-height: 44px;
  box-sizing: border-box;
  font-size: 14px;
  color: #fff;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;

  .title {
    float: left;
    font-size: 18px;
    margin-left: 13px;
    margin-right: 10px;
    padding: 0 5px;
    font-family: MFShangHei-Regular !important;
  }

  .nav {
    float: left;
    height: 44px;

    li.nav-item {
      float: left;
      padding: 0 5px;
      position: relative;
      cursor: pointer;
      text-transform: uppercase;

      &.active::after {
        display: block;
      }

      &::after {
        position: absolute;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-bottom: 7px solid #fff;
        content: " ";
        width: 2px;
        height: 0;
        top: 37px;
        left: 0;
        right: 0;
        margin: auto;
        display: none;
      }
    }
  }
}

.scenes-body {
  width: 100%;
  padding: 11px 10px 10px 10px;
  background-color: #fff;
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
  box-sizing: border-box;
  border-left: 1px solid #e5e5e5;
  border-right: 1px solid #e5e5e5;
  border-bottom: 1px solid #e5e5e5;

  .rows {
    margin: 0 auto;
  }

  .card {
    float: left;
    width: 33.3%;
    height: 314px;
    padding: 10px;
    box-sizing: border-box;
    background: #fff;
    transition: background-color 0.5s;

    .card-img {
      background: url(//p0.meituan.net/codeman/ae846a3….png) 50% 50%;
      background-size: cover;
      max-width: 100%;
      height: 208px;
      margin-bottom: 11px;
      cursor: pointer;

      img {
        border-radius: 4px;
      }
    }

    &:hover {
      background: #e5e5e5;
    }
  }

  .card-info {
    text-align: left;

    .title {
      font-size: 16px;
      color: #222;
      height: 22px;
      line-height: 22px;
      margin-bottom: 8px;
      font-weight: 500;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      cursor: pointer;
    }

    .tags {
      font-size: 12px;
      color: #999;
      height: 20px;
      overflow: hidden;
      margin-bottom: 5px;

      .tag {
        float: left;
        height: 18px;
        line-height: 18px;
        text-align: center;
        border: 1px solid #d8d8d8;
        border-radius: 2px;
        margin-right: 10px;
        margin-bottom: 5px;
        padding: 0 3px;
      }
    }

    .price {
      height: 27px;
      overflow: hidden;
      margin-bottom: 10px;
      color: rgb(179, 118, 6);
    }
  }
}

.bigger-style {
  background-color: rgb(190, 164, 116);
  background-image: linear-gradient(
    to right,
    rgb(194, 176, 142) 3%,
    rgb(190, 164, 116) 100%
  );
}
</style>
