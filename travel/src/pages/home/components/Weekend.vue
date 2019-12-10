<template>
  <div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl"/>
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
  </div>
</template>
<script>
export default{
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: "0001",
        imgUrl: "https://imgs.qunarzz.com/sight/source/1511/ea/7f43191b747bb9.jpg_r_640x214_f58e829d.jpg",
        title: "上海迪士尼乐园",
        desc: "上海迪士尼乐园很好玩"
      },{
        id: "0002",
        imgUrl: "https://imgs.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
        title: "上海迪士尼乐园",
        desc: "上海迪士尼乐园很好玩"
      },{
        id: "0003",
        imgUrl: "https://imgs.qunarzz.com/sight/source/1505/7b/2a6b0ce087f0e5.jpg_r_640x214_5c76b115.jpg",
        title: "上海迪士尼乐园",
        desc: "上海迪士尼乐园很好玩"
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img 
      width: 100%
  .item-info
    min-width: 0
    flex: 1
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
