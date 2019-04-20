<template>
  <div class="index">
    <banner-img />
    <top-menu />
    <content-list />
  </div>
</template>

<script>
import bannerImg from '@/views/bannerImg/banner.vue'
import topMenu from '@/views/topNav/topMenu.vue'
import contentList from '@/views/contentList/contentList.vue'

export default {

  components: {
    topMenu,
    bannerImg,
    contentList
  },
  data () {
    return {
    };
  }
}

</script>
<style lang='less' scoped>
</style>