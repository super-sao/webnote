<template>
  <div class="leftNav">
    <ul class="w100 h100">
      <li  v-for="(item,index) in leftNav" :key="index" @click="activeIndex = index">
        <div class="title">{{item.name}}</div>
        <div 
          :class="[
            'dropdown',
            activeIndex==index?'slide-in':'',
            activeSubIndex==index+'-'+inde?'active':'']
          "
          v-for="(ite,inde) in item.value"
          :key="inde"
          @click=" activeSubIndex = index+'-'+inde"
          >
          {{ite}}
        </div>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'home',
  data(){
    return{
      activeSubIndex:null,
      activeIndex: null,
       leftNav: [
         {
           name:"基础",
           value:["html","css","js"]
         },
         {
           name:"框架",
           value:["bootstrap","elementUI","layui"]
         },
         {
           name:"服务器",
           value:["nginx","apache","php"]
         }
       ]
    }
  },
  methods:{
 
  }
}
</script>
<style lang="less" scoped>
@mainColor: #006400;
@borderColor: #84ceaf;
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
    ul li{
      padding-left: 20px;
      margin-bottom: 10px;
      text-align: left;
      font-size:20px;
      &:hover{
        cursor:pointer
      }
      .title{
        font-weight: bold;
      }
      .dropdown{
        display:none;
        font-size:14px; 
        padding:6px 0;
        &.slide-in{
          display:block;
        }
        &.active{
          color:red;
        }
      }
    }
  }

</style>
