<template>
  <div class="left-nav">
    <ul>
      <li>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-gouwucheman"></use>
        </svg>
        <p>支付中心</p>
      </li>
      <li>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-dianpu"></use>
        </svg>
        <p>店铺</p>
      </li>
      <li>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-hanbao"></use>
        </svg>
        <p>商品</p>
      </li>
      <li>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-huiyuanqia"></use>
        </svg>
        <p>VIP会员</p>
      </li>
      <li>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-gongnengjianyi"></use>
        </svg>
        <p>账户设置</p>
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'leftnav',
  data () {
    return {}
  }
}
</script>

<style>
.left-nav{
  float: left;
  background: rgb(105, 144, 216);
  width: 5%;
  height: 100%;
  color:#fff;
  text-align: center;
}

/* 这个一定要知道，列表因为有列表项它前面是有空间的，要用这个使得左边没有空白 */
.left-nav ul{
  margin-left: 0;
  padding-left: 0;
}
.left-nav li{
  list-style: none;
}
.left-nav  svg{
  width:80%;
  font-size: 30px;
}
.left-nav li p{
  font-size: 12px;;
}
</style>
