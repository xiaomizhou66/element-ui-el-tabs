<template>
  <div class="pos">
    <el-row>
      <!-- 下面是中间点餐栏 -->
      <el-col :span="7">
        <div class="grid-content bg-purple-dark" style="border-right:1px solid gray;">
          <el-tabs>
            <el-tab-pane label="点餐">
              <el-table :data="tableData" border show-summary style="width: 100%;text-align:center;">
                <el-table-column prop="goodsName" label="商品"></el-table-column>
                <el-table-column prop="count" label="量" width="50"></el-table-column>
                <el-table-column prop="price" label="金额" width="70"></el-table-column>
                <el-table-column label="操作" width="100" fixed="right">
                  <template slot-scope="scope">
                    <el-button @click="handleClick(scope.row)" type="text" size="small">删除</el-button>
                    <el-button type="text" size="small">增加</el-button>
                  </template>
                </el-table-column>
              </el-table>
            </el-tab-pane>
            <div>
              <el-button type="warning">挂单</el-button>
              <el-button type="info">删除</el-button>
              <el-button type="success">结账</el-button>
            </div>
            <el-tab-pane label="挂单">
              挂单
            </el-tab-pane>
            <el-tab-pane label="外卖">
              外卖
            </el-tab-pane>
          </el-tabs>
        </div>
      </el-col>
      <!-- 下面是右边商品栏 -->
      <el-col :span="17">
        <el-row>
          <div class="grid-content bg-purple-light">
            <div class="recommended-goods">
              <div class="title">美食推荐</div>
              <div class="recommended-goods-list">
                <ul>
                  <li v-for="good in goods" :key="good.goodsId">
                    <span>{{ good.goodsName }}</span>
                    <span class=" o-price ">{{good.price}}</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </el-row>
        <!--  在下面这段代码编辑之前都没有问题， -->
        <el-row>
          <!-- 在这个div外面套一个el-row也解决了问题 -->
          <div class="goods-type">
            <!--  <h1>在这里加上这行可以解决问题</h1> -->
            <el-tabs :value="'name2'">
              <el-tab-pane label="汉堡" name="name1">
                111111111111111
              </el-tab-pane>
              <el-tab-pane label="小食" name="name2">
                2222222222222222222
              </el-tab-pane>
              <el-tab-pane label="饮料" name="name3">
                33333333333333
              </el-tab-pane>
              <el-tab-pane label="套餐" name="name4">
                4444444444444444444
              </el-tab-pane>
            </el-tabs>
          </div>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'pos',
  methods: {
    handleClick (row) {
      console.log(row)
    }
  },
  data () {
    return {
      tableData: [
        {
          goodsName: '可口可乐',
          price: 8,
          count: 1
        },
        {
          goodsName: '香辣鸡腿堡',
          price: 15,
          count: 1
        },
        {
          goodsName: '爱心薯条',
          price: 8,
          count: 1
        },
        {
          goodsName: '甜筒',
          price: 8,
          count: 1
        }
      ],
      goods: [
        {
          goodsId: 1,
          goodsName: '香辣鸡腿堡',
          price: 18
        },
        {
          goodsId: 5,
          goodsName: '脆皮炸鸡腿',
          price: 10
        },
        {
          goodsId: 6,
          goodsName: '魔法鸡块',
          price: 20
        },
        {
          goodsId: 7,
          goodsName: '可乐大杯',
          price: 10
        }
      ]
    }
  }
}
</script>

<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  display: block;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.title {
  height: 20px;
  border-bottom: 1px solid #d3dce6;
  background-color: #f9fafc;
  padding: 10px;
}
.recommended-goods-list ul li {
  list-style: none;
  float: left;
  /* 这里用了浮动没有清清除，导致崩溃 */
  border: 1px solid #e5e9f2;
  padding: 10px;
  margin: 5px;
  background-color: #fff;
}
/* .goods-type{
  clear: both;
} */
/* 清除了浮动就没有问题了 */
.o-price {
  color: #58b7ff;
}
</style>
