<template>
    <div class="list-box">
        <ul class="content">
            <li v-for="obj in rate" :key="obj.id" class="list">
                <div class="img-box">
                    <img :src="obj.portrait">
                </div>
                <div class="info-box">
                    <div class="basic">
                        <span class="name">{{obj.name}}</span>
                        <span class="date">{{obj.time}}</span>
                    </div>
                    <div class="time">{{obj.duration}}分钟</div>
                    <div class="desc">{{obj.content}}</div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props:["rate"]
    }
</script>

<style lang="scss" scoped>
.list-box{
    border-top:1px solid #e4e4e4;
    .content{
        padding: 0 0.3rem;
        .list{
            padding:0.3rem 0 0.2rem 0;
            display: flex;
            .img-box{
                width:0.8rem;
                flex:0 0 0.8rem;
                margin-right: 0.2rem;
                img{
                    width:100%;
                    border-radius: 50%;
                }
            }
            .info-box{
                flex:1;
                min-width: 0;
                .basic{
                    color:#2f2f2f;
                    font-size: 0.32rem;
                    .date{
                        color:#898989;
                        font-size: 0.24rem;
                        float: right;
                    }
                }
                .time{
                    color:#666;
                    font-size: 0.24rem;
                    margin-top: 0.14rem;                    
                }
                .desc{
                    line-height: 0.4rem;
                    color:#2f2f2f;
                    padding:0.28rem 0 0.16rem;
                }
            }
        }
    }
}
</style>