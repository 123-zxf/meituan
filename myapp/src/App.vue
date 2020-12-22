<template>
  <div id="app">
    美团外卖
    <!-- <router-link to="/home">首页</router-link> -->
    <!-- 此种方式传参会让参数 -->
    <router-link :to="{name:'home',params:{name:'张三',age:10}}">首页</router-link>
    <!-- <router-link to="/mine">我的</router-link> -->

    <!-- 通过query传参，这种方式参数会在地址栏。而且刷新页面不会消失 -->
    <router-link :to="{path:'/mine',query:{name:'李四',age:10}}">我的</router-link>
    
    <!-- 通过路径跳转传参 -->
    <!-- <router-link to="/mine/zs/12">我的</router-link> -->
    <router-view></router-view>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
