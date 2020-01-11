<template>
  <div id="content">
    <header>
      <div class="logoWrap">
        <img src="../assets/fontLogo.png" alt="logo" />
      </div>
      <div class="topNav">
        <ul class="topNavBox">
          <li
            @click="change(item)"
            :class="[topNavType==item?'topNavType':'']"
            :key="index"
            v-for="(item,index) in topNav"
          >
            {{item}}
            <!-- <router-link :to="'/leftNav/'+item"></router-link> -->
          </li>
        </ul>
      </div>
    </header>

    <!-- <router-view class="aaa"></router-view> -->
    <div class="leftNav">
      <div
        class="leftNavBox"
        style="height:42px"
        @click.stop="sfq(index,$event)"
        @mouseover="sfqON(index)"
        @mouseout="sfqOFF(index)"
        v-for="(item, index) in leftNav"
        :key="index"
        :ref="`list${index}`"
        :data-innerText="item[0]"
        data-type="off"
      >
        <h3>{{item[0]}}</h3>

        <div class="leftNavBoxList" v-for="(item, index) in item[1]" :key="index">
          <span @click="test(item)">{{item}}</span>
        </div>
      </div>
    </div>
    <div class="rightContent"></div>
  </div>
</template> 

<script>
//  引进组件
// import Content from "./views/Content";

export default {
  //  数据
  data() {
    return {
      topNav: [
        "HTML",
        "CSS",
        "JavaScript",
        "Vue",
        "React",
        "WeChatApp",
        "Node",
        "Git",
        "Linux"
      ],
      leftNav: [
        [
          "基础",
          [
            "<!DOCTYPE>",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "格式",
          [
            "<!DOCTYPE>",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "表单",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "框架",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "图像",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "音频/视频",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "链接",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "列表",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "表格",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "样式/节",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "编程",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ],
        [
          "元信息",
          [
            "<!DOCTYPE> ",
            "<html>",
            "<title>",
            "<body>",
            "<h1> to <h6>",
            "<p>",
            "<br>",
            "<hr>",
            "<!--...-->"
          ]
        ]
      ],
      topNavType: "HTML",
      leftNavType: "基础",
      leftNavItem:""
    };
  },

  //  接受数据
  props: {},

  //  函数主体
  methods: {
    change(topNavType) {
      this.topNavType = topNavType;
    },

    sfq(index, event) {
      this.leftNavType = this.$refs[`list${index}`][0].dataset.innertext
      if (
        event.target.innerText ===
        this.$refs[`list${index}`][0].dataset.innertext
      ) {
        if (this.$refs[`list${index}`][0].dataset.type == "off") {
          this.$refs[`list${index}`][0].style.cssText = "height: auto;";
          this.$refs[`list${index}`][0].dataset.type = "on";
        } else {
          this.$refs[`list${index}`][0].style.cssText = "height: 42px;";
          this.$refs[`list${index}`][0].dataset.type = "off";
        }
      } else {
        this.$refs[`list${index}`][0].style.cssText = "height: auto;";
        this.$refs[`list${index}`][0].dataset.type = "on";
      }
      window.console.log(this.topNavType,this.leftNavType,this.leftNavItem)
    },

    sfqON(index) {
      this.$refs[`list${index}`][0].style.cssText = "height: auto;";
    },

    sfqOFF(index) {
      if (this.$refs[`list${index}`][0].dataset.type == "off") {
        this.$refs[`list${index}`][0].style.cssText = "height: 42px;";
      }
    },
    test(a){
      this.leftNavItem = a
    }
  },

  //  计算属性
  computed: {},

  //  侦听器
  watch: {
    "$route.path": function(to, from) {
      window.console.log(to);
      window.console.log(from);
    }
  },

  //  注册组件
  components: {
    // Content
  },

  //  自定义指令
  directives: {},

  //  过滤器
  filters: {}
};
</script>


<style lang="less">
@mainColor: #006400;
@borderColor: #84ceaf;
#content {
  & > header {
    // background-color: #aaa;
    display: flex;
    justify-content: space-between;
    // height: 60px;
    position: relative;
    top: 0;
    border-bottom: 1px solid #ebebeb;

    .logoWrap {
      img {
        display: block;
        height: 40px;
        margin: 10px 30px;
        // cursor: pointer;
      }
    }
    .topNavBox {
      display: flex;
      li {
        line-height: 56px;
        margin-right: 20px;
        cursor: pointer;
        border-top: 2px solid transparent;
        border-bottom: 2px solid transparent;
      }
      li:hover {
        position: relative;
        left: 2px;
        border-bottom: 2px solid @mainColor;
      }
      .topNavType {
        border-bottom: 2px solid @mainColor;
      }
    }
  }

  .leftNav {
    position: absolute;
    width: 200px;
    top: 60px;
    left: 0px;
    bottom: 0px;
    overflow-x: hidden;
    overflow-y: auto;
    // background-color: #aaa;
    border-right: 1px solid #f1f1f1;
    .leftNavBox {
      margin-right: 40px;
      margin-left: 20px;
      overflow: hidden;
      // height: auto;
      // border: 1px solid #000;

      h3 {
        margin: 8px 0px;
        cursor: pointer;
      }
      .leftNavBoxList {
        // padding: 2px;
        cursor: pointer;
        span {
          display: inline-block;
          padding: 4px 0px 2px 0px;
          margin-bottom: 2px;
          border-bottom: 2px solid transparent;
        }
        &:hover span {
          display: inline-block;
          border-bottom: 2px solid @borderColor;
        }
      }
    }
    // & > .leftNavBox:hover {
    //   height: auto;
    // }
  }
}
.shqON {
  animation: sfqON 0.2s linear 1;
}
@keyframes sfqON {
  0% {
    height: 42px;
  }
  100% {
    height: auto;
  }
}

@keyframes sfqOFF {
  0% {
    height: auto;
  }
  100% {
    height: 42px;
  }
}
</style>
