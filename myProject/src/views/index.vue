<template>
  <div class="index">
    <span>index</span>
    <topMenu></topMenu>
  </div>
</template>

<script>
import topMenu from '@/views/topNav/topMenu.vue'
export default {

  components: {
    topMenu: topMenu
  },
  data () {
    return {
    };
  }
}

</script>
<style lang='less' scoped>
</style>