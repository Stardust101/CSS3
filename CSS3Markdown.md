##  CSS3的一些常用特效

### 我所学习到CSS3的一些属性 也是用过的  简单做一下分享

### 元素的阴影  (我们可以为文本 也可以盒子添加一个阴影)

#### 1.为文本添加阴影，使用属性text-shadow
        例如：text-shadow:1px 1px 1px red;
            1:第一个参数
                代表的影子的水平偏移位置，如果是正数，水平向右，如果是负数，水平向左
            2：第二个参数
                代表的是影子垂直方向的偏移位置，如果是正数，垂直向下，如果是负数，垂直向上。
            3：第三个参数
                代表的是模糊度，不能是负数，值越大，模糊度越高
            4：第四个参数
                代表的是影子的颜色
#### 2.为文本添加阴影，使用属性 box-shadow ，我们可以为盒子添加阴影

            1:第一个参数
                代表的影子的水平偏移位置，如果是正数，水平向右，如果是负数，水平向左
            2：第二个参数
                代表的是影子垂直方向的偏移位置，如果是正数，垂直向下，如果是负数，垂直向上。
            3：第三个参数
                代表的是模糊度，不能是负数，值越大，模糊度越高
            4：第四个参数
                代表的是影子的颜色
#### 3. 我们可以为盒子，以及文本添加多一个阴影，以逗号隔开
        例如：box-shadow:1px 1px 1px red，1px 1px 1px red;
        我们可以为盒子设置内阴影 ，多个内阴影
        box-shadow:inset 1px 1px 1px red，inset 1px 1px 1px red;
        影子不会占位置，只是用来显示，我们可以为盒子添加影子，让页面有立体感效果。
        
##  边框圆角
        我们使用的是border-radius 属性
        例如：border-radius：10px;
        代表的是四个角的水平方向的距离是10px ，垂直方向的距离也是10px
        例如：border-radius:10/20px;
        代表的是四个角的水平方向的距离是10px ，垂直方向的距离也是20px
        例如：border-radius:10px 20px;
        第一个值:左上角以及右下角的水平以及垂直的距离都是10px
        第二个值：右上角以及左下角的水平以及垂直的距离都是20px
        例如：border-radius:10px 20px 30px 40px/20px 20px 30px 50px;
        第一个角的水平距离是10px，垂直的距离是20px
        第二个角的水平的距离是20px 垂直的距离20px
        第三个角的水平的距离是30px 垂直的距离也是30px
        第四个角的水平的距离是40px 垂直的距离也是50px
        
##  渐变：

####    1.线性渐变：(一个中心点沿着一个方向进行渐变)
          
        1:渐变的角度
        2：起始颜色
        3：终止颜色
        background-image：linear-gradient(
            to left,(使用度数来控制渐变的方向，这样会比较细致一些)
            yellow,
            green
        )
        渐变的位置
        background-image：linear-gradient(
            to left,(使用度数来控制渐变的方向，这样会比较细致一些)
            0% yellow ,
            25% green,
            50% yellow
        )
####    2.径向渐变：(一个中心点沿着四周的方向进行一个渐变)

        1：中心点的位置
        2：有一个半径
        3：起始颜色
        4：终止颜色
        background:radial-gradient(
                100px at 100px 100px,
                yellow,
                green
        )
        透明的球体 （还利用了一些上午rgba ）
##  过度：(过渡也是我们常用到的属性之一，我们可以做一些变换,有四个属性)
       transtion:all 1s ease 0;
       transition-property:all(过度的执行transition效果)
       transition-duration:1s(过度的时间)
       transition-timing-function：ease（过度的速率）
       transition-delay:0;(过度的延迟时间)
       过度是css3当中动画的一种，补间动画 （动画）
       需要有一个起始状态，然后一个终止态度，不用管中间的状态。
       transtion：all 1s；
##     2d转换 3d转换是css3 具有颠覆性的特征之一  也是我们经常会使用到的属性
###  　　2d：
       使用的transform属性
       我们可以使用2d 来完成那些效果
       scale 在当前元素的基础上进行缩放，放大到原来的一倍，缩小到原来的一个，水平方向进行缩放，垂直方向进行缩放
       scale(1,2);
       translate
       在当前元素的当前位置的基础上进行移动。
       可以进行水平方向上面的移动，
       transate(水平,垂直)
       100px   200px
       -100px, -200px
       百分比
       可以进行垂直方向上面的移动
       rotate
       旋转
       1：角度
          顺时针方向
          rotate（30deg）
       2：旋转的中心点
           我们默认是当前元素的中心位置
          我们可以对这个位置进行更改
           transform-origin:left center;
           transform-origin:100px 100px;
           transform-origin:0% 100%;

我们要注意一个细节：2d transform 是一般是配合过度一起使用才能完成一些动画效果。

###  学习了2d转换 ，缩放，我们接下来看看3d
    移动
           x 轴，水平方向移动
           y 轴，垂直方向移动
    旋转
           rotate(360deg)   顺时针方向。实际上围绕z 轴在转。

### 3d
    1：明确3d 坐标系，明确x  y ，z 轴的正负方向
    2：围绕x 轴怎么旋转，围绕y  轴，怎么选择，z 怎么旋转
    假设以x 轴旋转，你把x 轴的正方向对着你，正角度，就是顺时针方向，负角度就是逆时针方向。
    3：旋转默认是在当前元素或者盒子的中心点的位置旋转
    4：旋转是整个坐标系发生表，旋转的是一个坐标系。
    5：每个盒子，每一个面都对应一个3d 坐标系。
###  透视：
    3d加上透视是比较好的效果。
    目前浏览器都不支持 perspective 属性。
    Chrome 和 Safari 支持替代的 -webkit-perspective 属性。
    没有透视之前，我们的这些旋转原本是在一个2d 的平面
    我们看到的效果有一些堆叠的效果。
    我加透视：调整观察者与目标物的距离，就能够实现，在一个2d 的平面呈现出3d 效果。

##  动画也是我们常用的属性 animation  它一共有8个属性
          animation-name:我要使用的动画的名称;
          animation-duration:持续时间
          animation-timing-function:动画的只是速度的方式
          animation-delay 动画的延迟时间
          animation-iteration-count:执行动画的次数
          animation-direction: nomarl,reverse,alternate;
          animation-fill-mode:动画的状态，执行动画之后的状态是开始状态，还是结束状态
          animation-play-state: 动画的状态。
          
    定义动画：
         @keyframes change{
                0%{
                     width:200px
                }
                10%{
                     width:400px;
                }
                100%{

                }
         }

    使用动画：
      animation:change 1s linear inifite;
      
####  下节跟大家具体分享flex弹性盒子布局的相关知识  这个也是一件web开发的利器。
