
##bootstrap

###1.modal插件：
```javascript
   $('#myModal').modal(options)
   options ={
       backdrop: true,//true,false,"static"  点击mask背景时关闭模态框。
       keyboard: true, //true,false          键盘上的 esc 键被按下时关闭模态框。
       show:true, //true,false               模态框初始化之后就立即显示出来。
       remote:"path" //path为远程服务器路径，
                    //如果提供的是 URL，将利用 jQuery 的 load 方法从此 URL 地址加载要展示的内容（只加载一次）并插入 .modal-content 内。
                    // 如果使用的是 data 属性 API，还可以利用 href 属性指定内容来源地址
   }
   .eg:
   <a data-toggle="modal" href="remote.html" data-target="#modal">Click me</a>
```
