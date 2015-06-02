## SVG 形状
SVG 有一些预定义的形状元素，可被开发者使用和操作：
* 矩形(**rect**)     **`<rect x y width height rx ry style >`** 
* 圆形(**circle**)   **`<circle cx cy r >`**
* 椭圆(**ellipse**)
* 线(**line**)
* 折线(**polyline**)
* 多边形(**polygon**)
* 路径(**path**)
* [锚点](#123):


更多信息见w3school的[SVG教程](http://www.w3school.com.cn/svg/index.asp "")... 

---
####[id="123"]矩形
~~~html
  <rect x="0" y="10" rx="15" ry="15" width="300" height="100" 
   style="fill:rgb(0,0,255);stroke-width:1;stroke:rgb(0,0,0);opacity:0.9;"/>
~~~
   + x,y：位置；width,height：宽高；rx,ry：圆角的椭圆半径
   + style 属性用来定义 CSS 属性
   + CSS 的 stroke-width 属性定义矩形边框的宽度
   + CSS 的 stroke 属性定义矩形边框的颜色
   + [123]: http://example.com/  "Optional Title Here"
   + [id]:(http://example.com/) "Optional Title Here"
   + Use the `<printf()>` function.

####圆形
~~~html
  <circle cx="100" cy="50" r="40" stroke="black" stroke-width="2" fill="red"/>
~~~
   + cx,cy:圆点的x和y坐标。如果省略 cx 和 cy，圆的中心会被设置为 (0, 0)
   + r 属性定义圆的半径。
     
####椭圆
~~~html
  <ellipse cx="300" cy="150" rx="200" ry="80" style="fill:rgb(200,100,50);stroke:rgb(0,0,100);stroke-width:2"/> 
~~~
   + cx,cy:圆点的x,y坐标
   + rx,ry:水平半径,垂直半径
   
####线
~~~html
  <line x1="0" y1="0" x2="300" y2="300" style="stroke:rgb(99,99,99);
     stroke-width:2"/> 
~~~
   + x1,y1 定义线条的开始坐标
   + x2,y2 定义线条的结束坐标
   
####折线
~~~html
   <polyline points="0,0 0,20 20,20 20,40 40,40 40,60" style="fill:white;stroke:red;stroke-width:2"/>
~~~
   + points 定义折线每个点的 x 和 y 坐标

####多边形
~~~html
  <polygon points="220,100 300,210 170,250" style="fill:#cccccc;
     stroke:#000000;stroke-width:1"/>
~~~
   + points 定义多边形每个角的 x 和 y 坐标  
   
####路径
    <path> 标签用来定义路径。
    下面的命令可用于路径数据：
    - M = moveto
    - L = lineto
    - H = horizontal lineto
    - V = vertical lineto
    - C = curveto
    - S = smooth curveto
    - Q = quadratic Belzier curve
    - T = smooth quadratic Belzier curveto
    - A = elliptical Arc
    - Z = closepath
    

注释：以上所有命令均允许小写字母。大写表示绝对定位，小写表示相对定位。
  
  + 下面的例子定义了一条路径，它开始于位置 250 150，到达位置150 350，然后从那里开始到 350 350，最后在 250 150 关闭路径。
  ~~~html
  <path d="M250 150 L150 350 L350 350 Z" />
  ~~~
  
  + 下面的例子创建了一个螺旋
~~~html
    <?xml version="1.0" standalone="no"?>
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
    "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
    <svg width="100%" height="100%" version="1.1"
    xmlns="http://www.w3.org/2000/svg">
        <path d="M153 334
        C153 334 151 334 151 334
        C151 339 153 344 156 344
        C164 344 171 339 171 334
        C171 322 164 314 156 314
        C142 314 131 322 131 334
        C131 350 142 364 156 364
        C175 364 191 350 191 334
        C191 311 175 294 156 294
        C131 294 111 311 111 334
        C111 361 131 384 156 384
        C186 384 211 361 211 334
        C211 300 186 274 156 274"
        style="fill:white;stroke:red;stroke-width:2"/>
    </svg>
~~~
---