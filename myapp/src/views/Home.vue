<template>
    <div>
        <button @click="$router.go(-1)">返回</button>
        <button @click="go()">我的页面</button>
        我是首页{{$route.params.name}}{{$route.params.age}}
        <router-link to="/home/test1">test1</router-link>
        <router-view></router-view>
    </div>
</template>

<script>
    export default {
        methods: {
            go(){
                this.$router.push({path:'/mine',query:{name:"王五",age:17}})
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>