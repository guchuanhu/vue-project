<template>
  <div id="app">
    <div class="log">
      <img src="./assets/log.png"/>
    </div>
    <div class="menu">
      <ul>
        <li v-for="item in menu" :key=item.c>
          <router-link :to="item.href">
            <div>{{item.c}}</div>
            <div class="little">{{item.e}}</div>
          </router-link>
        </li>
      </ul>
    </div>
    <div class="container">
      <router-view/>

      <div class="footer">
        <div class="top">
          <img class="f1" src="./assets/fo.png" />
          <p>总部地址：河北省秦皇岛市海港区 海阳路与红旗路交叉口215-1号</p>
          <p>投资热线：400-0335-608</p>
          <img class="f2" src="./assets/fot.png" />
        </div>
        <div class="bottom">
          <div class="left">
            <img src="./assets/wx.png" />
            <span>微信公众号</span>
          </div>
          <div class="left">
            <img src="./assets/wb.png" />
            <span>微博官网</span>
          </div>

          <div class="right">产品展示</div>
          <div class="right">品牌介绍</div>
          <div class="right">最新动态</div>
          <div class="right">返回顶部</div>
        </div>
      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      menu: [
        {'c': '首页','e': 'Home page','href': "/"},
        {'c': '关于','e': 'With regard to','href': "list"},
        {'c': '美食体验','e': 'Food experience','href': "/"}
        ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
}
*{margin: 0;padding: 0}
a{    
  color: #333;
  text-decoration: none;
  }
.log{
  padding: 50px 0;
  background-color: #f6bb41;
}
.log img{
  width: 100px;
}
.menu{
  padding: 30px 0;
  background: url("./assets/bg1.png");
}
.menu ul{
  list-style: none;
}
.menu ul li{
  display: inline-block;
  margin-right: 30px;
}
.menu ul li .little{
  font-size: 10px;
}
.container{
  background: url("./assets/bg2.png");
}
.footer{
    position: relative;
    max-width: 700px;
    margin: auto;
}
.footer .top{
    text-align: left;
    padding: 20px 30px;
    background-color: white;
}
.footer .top .f1{
    width: 120px;
}
.footer .top .f2{
    width: 60px;
    position: absolute;
    top: 9px;
    right: 30px;
}
.footer .top p{
    display: block;
    margin-top: 15px;
    font-size: 12px;
}
.footer .top p:last-child{
    display: block;
    margin-top: 0;
    margin-bottom: 5px;
}
.footer .bottom{
  padding: 15px 50px;
  color: white;
  background-color: #313131;
}
.footer .bottom:after{
  content: "";
  display: block;
  clear: both;
}
.footer .bottom .left{
      width: 132px;
          height: 20px;
    text-align: left;
  white-space: nowrap;
  float: left;
  position: relative;
}
.footer .bottom .left img{
  width: 26px;
}
.footer .bottom .left span{
  font-size: 13px;
  position: absolute;
  top: 2px;
    left: 30px;
}
.footer .bottom .right{
  float: right;
      font-size: 12px;
    margin-left: 20px;
}
</style>
