<template>
  <div class="tag-box">
    <span v-for="obj in tag" :key="obj.id" class="tag-item" @click="changeTab(obj.id)" :class="{'active':currentType==obj.id}">{{obj.name}}（{{obj.count}}）</span> 
  </div>
</template>

<script>
export default {
  props:["tag","currentType"],
  methods: {
    changeTab(id){
      this.$emit('change',id)
    }
  }
};
</script>

<style lang="scss" scoped>
    .tag-box{
        padding:0.3rem 0.28rem 0.1rem;
        .tag-item{
            padding:0 0.24rem;
            display: inline-block;
            height: 0.52rem;
            line-height: 0.52rem;
            text-align: center;
            font-size: 0.26rem;
            color:#666;
            margin:0 0.2rem 0.2rem 0;
            border-radius: 0.52rem;
            border:1px solid #bbb;
            &.active{
              border:1px solid #ffb000;
              background:#fffbf1;
            }
        }
    }
</style>
