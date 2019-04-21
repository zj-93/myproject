<template>
  <div id="index" class="index" @touchstart="start" @touchmove="move" @touchend="end">
    <banner-img />
    <top-menu />
    <recommended-list/>
    <content-list :scroll-state="scrollState" :content-list="contentList" />
  </div>
</template>

<script>
import list from "@/views/json/list2.json"
import bannerImg from '@/views/bannerImg/banner.vue'
import topMenu from '@/views/topNav/topMenu.vue'
import contentList from '@/views/contentList/contentList.vue'
import recommendedList from '@/views/recommended/recommendedList.vue'

export default {
  components: {
    topMenu,
    bannerImg,
    contentList,
    recommendedList
  },
  data () {
    return {
      scrollState: '0',
      flag: true,
      contentList: [],
      list: []
    };
  },
  mounted() {
    this.list = list
    var _this = this
    setTimeout(() => {
      window.addEventListener('scroll', function(e){
        var BodyH = document.body.clientHeight
        var viewH = window.screen.height
        var scrollH = document.documentElement.scrollTop||document.body.scrollTop
        if(BodyH - viewH -scrollH == '0' && _this.flag) {
          _this.scrollState = '1'
          _this.queryContentListData()
        }
      })
    }, 300)
  },
  methods: {
    queryContentListData() {
      this.scrollState = '1'
      this.contentList = []
      var i = Math.floor(Math.random() * 10)
      if(i>1){
        this.queryContentListData()
      }else if(i <= 1){
        if(i== 1) {
          this.scrollState = '0'
          this.contentList= this.list
          this.flag = true
          console.log(this.contentList , this.list)
        }else{
          this.contentList = []
          this.scrollState = '2'
          this.flag = false
        }
      }
      console.log(i)
      console.log(this.contentList)
      this.$message({
        message: '请求数据',
        type: 'success'
      })
    },
    start() {
      console.log('移动开始')
    },
    move() {
      console.log('移动中')
    },
    end() {
      console.log('移动结束')
    }
  }
}

</script>
<style lang='less' scoped>
</style>