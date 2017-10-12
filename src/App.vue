<template>
  <div id="app">
    <div class='demo'>我是scss编译出来的语法</div>

    <ul>
    	<li>1.vue init webpack vue-scss</li>
		<li>2.cd vue-scss</li>
    	<li>3.npm install</li>
    	<li>4.npm install node-sass sass-loader -D</li>
    	<li>5.npm run dev</li>
    </ul>

    新的脚手架的都是配置好的，只需要的下载相应的laoder即可

  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang='scss'>

  @import './assets/style/normalize.scss';
  @import './assets/style/reset.scss';
  @import './assets/style/mixin.scss';
  @import './assets/style/func.css';


  body {
    font-size:0.28rem;/*设置主体的字体大小*/
  }

  #app {
   .demo {
    color:red;  /*scss的语法*/
   }
}




</style>
