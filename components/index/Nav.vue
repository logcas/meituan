<template>
    <div class="nav">
        <div class="center-container">
            <div class="nav-header nav-style">
                <span class="title">美团导航</span>
            </div>
            <div class="nav-body clearfix">
                <div class="nav-content clearfix" v-for="(item,key) in items" :key="key">
                    <div class="nav-title">{{ item.name }}</div>
                    <ul class="nav-list">
                        <li class="nav-list-item" v-for="(city,idx) in item.childs" :key="idx">
                            <nuxt-link :to="city.link">{{ city.name }}</nuxt-link>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
        items:[
            {
                name: '热门城市',
                childs: [
                    {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                    {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                ]
            },
            {
                name: '热门服务',
                childs: [
                    {
                        name: '酒店',
                        link: '/city/zhengzhou'
                    },
                    {
                        name: '健身体育',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '亲子',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                ]
            },
            {
                name: '周边服务',
                childs: [
                    {
                        name: '这里是周边服务',
                        link: '/city/zhengzhou'
                    },
                    {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                                        {
                        name: '郑州',
                        link: '/city/zhengzhou'
                    },
                ]
            }
        ]
    };
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
$basicColor: #31bbac;

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

.nav {
  width: 100%;
  background: #f4f4f4;
}

.center-container {
  margin: 0 auto;
  margin-top: 40px;
  width: 1190px;
}

.nav-header {
  height: 44px;
  line-height: 44px;
  box-sizing: border-box;
  font-size: 14px;
  color: #fff;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;

  .title {
    float: left;
    font-size: 16px;
    margin-left: 13px;
    margin-right: 10px;
    padding: 0 5px;
    font-family: MFShangHei-Regular !important;
  }
}

.nav-body {
  width: 100%;
  padding: 0;
  background-color: #fff;
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
  box-sizing: border-box;
  border-left: 1px solid #e5e5e5;
  border-right: 1px solid #e5e5e5;
  border-bottom: 1px solid #e5e5e5;
}

.nav-style {
  background-color: #0ecac7;
  background-image: linear-gradient(-90deg, #0ecac7 0, #06c1ae 100%);
}

.nav-content {
  .nav-title {
    width: 100px;
    height: 100%;
    float: left;
    font-size: 14px;
    font-weight: 500;
    color: #222;
    text-align: center;
    padding: 10px 0;
  }

  .nav-list {
    width: 1080px;
    height: auto;
    padding-top: 12px;
    float: left;
    border-bottom: 1px solid #e5e5e5;
    overflow: hidden;

    .nav-list-item {
      width: 100px;
      height: 17px;
      font-size: 12px;
      text-align: left;
      margin-bottom: 13px;
      float: left;

      a {
          color: #666;
      }

      a:hover {
        color: $basicColor;
      }
    }
  }
}
</style>
