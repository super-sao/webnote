<template>
  <div id="app" class="w100 h100">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/content">About</router-link>
    </div>
    <router-view/>-->
    <!-- <Content></Content> -->
    <router-view />
  </div>
</template>
<script>
//  引进组件
import Content from "./views/Content";

export default {
  //  数据
  data() {
    return {};
  },

  //  接受数据
  props: {
    // parentData: {
    //   type: Object,
    //   default: () => {}
    // }
  },

  //  函数主体
  methods: {},

  //  计算属性
  computed: {},

  //  侦听器
  watch: {},

  //  注册组件
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Content
  },

  //  自定义指令
  directives: {},

  //  过滤器
  filters: {}
};
</script>


<style lang="less">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.clear::after {
  content: "";
  display: block;
  clear: both;
  visibility: hidden;
  overflow: hidden;
  height: 0;
}

* {
  margin: 0;
  padding: 0;
  list-style: none;
  color: #000;
  text-decoration: none;
}
.w100{
  width: 100%;
}
.h100{
  height: 100%;
}
</style>
