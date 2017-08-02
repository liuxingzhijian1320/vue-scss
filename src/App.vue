<template>
  <div id="app">
    <div class='demo'>我是scss编译出来的语法</div>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang='scss'>
  body {
    font-size:0.28rem;/*设置主体的字体大小*/
  }

  #app {
   .demo {
    color:red;  /*scss的语法*/
   }
}
</style>
