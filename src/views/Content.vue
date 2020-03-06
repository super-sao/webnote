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
    <leftNav />

    <div class="rightContent">
      <!-- <div id="main">
        <mavon-editor v-model="value" @change="xx" />
      </div> -->
      <div class="markdown-body markdown-box" v-html="value">{{value}}</div>
    </div>
  </div>
</template> 

<script>
//  引进组件
import leftNav from "@/components/leftNav.vue";
import "../css/github-markdown.min.css";

export default {
  components: {
    leftNav
  },
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
      leftNavItemType: "",
      value: `<p>所谓路由，可以理解成映射，就是两种食物之间的对应关系。至于express的路由呢，就是指URL和后端处理代码的对应关系，其作用就是将请求分发到对应的处理函数中。</p>
<h4><a id="1__2"></a>1. 应用级路由</h4>
<pre><div class="hljs"><code class="lang-js"><span class="hljs-comment">// 导入express模块</span>
<span class="hljs-keyword">const</span> express = <span class="hljs-built_in">require</span>(<span class="hljs-string">'express'</span>);
<span class="hljs-comment">// 基于express创建服务器</span>
<span class="hljs-keyword">const</span> app = express();`,
      // markdownOption: {

      //   subfield: true, // 单双栏模式
      //   preview: true // 预览
      // }
      // markdownOption: {
      //   subfield: false,

      // },
      editableType: false
    };
  },

  //  接受数据
  props: {
    // subfield: false
  },

  //  函数主体
  methods: {
    xx(a, b) {
      // eslint-disable-next-line no-console
      console.log(b);
      this.value = b;
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
.rightContent {
  // width: calc(100% - 200px);
  position: absolute;
  right: 0;
  top: 60px;
  bottom: 0px;
  left: 200px;
  // overflow: auto;
}
.markdown-box{
  padding:20px 50px;
}
</style>
