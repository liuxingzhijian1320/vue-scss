> A vue-scss-ip template
### 本模板功能包括：scss语编译，本机的ip显示，rem布局

> A Vue.js project

1. vue init webpack vue-douyu

2. cd vue-douyu

3. npm install

4. npm run dev

5. 打开build/webpack.base.config.js
```
alias: {
      'vue$': 'vue/dist/vue.esm.js',
      'src': resolve('src'),
      'assets': resolve('src/assets'),
      'components': resolve('src/components'),
      'views': resolve('src/views'), //src 创建view是的目录
    }
```

6. 新建 src/assets/script/rem.js
 ```
 export const rem = function () {
   function setFontSize(mw, mh, tw, th) {
     // 设备宽高
     let deviceWidth = document.documentElement.clientWidth;
     let deviceHeight = document.documentElement.clientHeight;
     let fontSize = 1;
     calSize();

     function calSize() {
       deviceWidth = document.documentElement.clientWidth;
       deviceHeight = document.documentElement.clientHeight;
       if (deviceWidth < 1080) {
         fontSize = deviceWidth / mw * 100;
       } else {
         fontSize = deviceWidth / mw * 100;
       }
       document.documentElement.style.fontSize = `${fontSize}px`;
     }
     window.addEventListener('resize', (event) => {
       calSize();
     });
   }
   setFontSize(375*2, 667*2, 768*2, 1024*2);
 };
 ```
 //main.js
 ```
 //rem.js
 import { rem } from 'assets/script/rem'; // rem
 rem();
 ```


 7. index.html
  ```
   <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  ```

 8. 添加ip的插件
   ```
   npm install ip -D

   ```

   - build  / dev-server.js 添加代码

   ```
   const ip = require('ip')
   const IP = ip.address();

   ```

   ```
   原先的 const uri = 'http://localhost:' + port 改成 var uri = `http://${IP}:${port}`;

   ```

 9. 修改端口号 config／index.js  将8080 的 端口号的改为 6788（任意修改，80端口的经常冲突）


 10. laoder
  ```
  npm install node-sass sass-laoder -D

  ```

  11. css 初始化
   //main.js(对应的scss到style的文件夹查看，这里不展示)
   ```
    @import './assets/style/normalize.scss';
     @import './assets/style/reset.scss';
     @import './assets/style/mixin.scss';
     @import './assets/style/func.css';

```



For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
```
# scss config check url
http://blog.csdn.net/zhooson/article/details/63682280

# favicons-webpack-plugin config check url
http://blog.csdn.net/zhooson/article/details/70336246

# ip config check url
http://blog.csdn.net/zhooson/article/details/74389211
```
