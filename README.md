# element-ui-el-tabs
element-ui-el-tabs 

# 运行
### install dependencies
npm install

### serve with hot reload at localhost:8080
npm run dev



# 遇到的问题：使用的el-tabs组件之后npm run dev页面崩溃了。

目前的代码，
分成左导航leftnav，与右边商品订单栏class=main，商品订单栏class=main又分为订单栏、商品区，
使用的是float布局。

在编辑商品区el-tabs的之后就出错了。代码在src/components/pagevue/pos.vue，图如下
![avatar](./src/assents/bug.png)


