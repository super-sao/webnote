<template>
  <div class="home">
   <button class="homeBtn" @click="$router.push('/content')">Markdown</button>
  </div>
</template>

<script>

export default {
  name: 'home',
}
</script>
<style lang="less" scoped>
.home{
  width:100%;
  height: 100%;
  text-align: center;
}
.homeBtn{
  width:400px;
  height: 80px;
  background: #0a6a0a;
  border-radius: 8px;
  margin: 300px auto;
  border: none;
  color:white;
  font-size:20px;
  
}
</style>
