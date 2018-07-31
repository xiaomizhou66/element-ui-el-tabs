# element-ui-el-tabs
element-ui-el-tabs 

# 运行
### install dependencies
npm install

### serve with hot reload at localhost:8080
npm run dev


###目前的代码布局
分成左导航leftnav，与右边商品订单栏div class=main，商品订单栏class=main又分为订单栏、商品区，
使用的是float布局。


### 遇到的问题：使用的el-tabs组件之后npm run dev页面崩溃了。已经用两个办法莫名其妙的解决了，但是不知道是为什么。
在编辑商品区el-tabs的之后就出错了。问题代码在src/components/pagevue/pos.vue，图如下
![avatar](./src/assents/bug.png)

### 解决办法
方法1：在el-tabs 前面加上一个标题行<h1>在这里加上这行行可以解决问题</h1> 就解决问题，
      但是很莫名其妙的不知道是怎么导致的，怎么解决的。
方法2：在el-tabs 外层再加上一个组件嵌套，<el-row></el-row> 也可以解决问题。
      但是也是特别莫名其妙的不知道是怎么导致的，怎么解决的。
