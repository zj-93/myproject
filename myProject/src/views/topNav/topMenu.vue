<template>
  <div class="menu">
      <div class="menuList">
          <ul>
              <li>
                <i class="icon1"></i>
                <span class="menuName">美食</span>
              </li>
              <li>
                <i class="icon4"></i>
                <span class="menuName">饮品</span>
              </li>
              <li>
                <i class="icon3"></i>
                <span class="menuName">水果</span>
              </li>
              <li>
                <i class="icon2"></i>
                <span class="menuName">旅游</span>
              </li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
  name: 'sss',
  data () {
    return {
        menuList: []
    };
  }
}

</script>
<style lang='less' scoped>
  .menu{
      padding-bottom: 20px;
      padding-top: 20px;
      box-sizing: border-box;
      background-color: #fff;
      border-top: 1px solid #ccc;
      margin-bottom: 20px;
    ul{
      display: flex;
      li{
        display: inline-block;
        flex: 1;
        text-align: center;
        cursor: pointer;
        .icon1{
          display: inline-block;
          height: 60px;
          width: 60px;
          background-image: url('~@/assets/img/icon1.png');
          background-repeat: repeat;
          background-position: center center;
          background-size: cover;
        }
        .icon2{
          display: inline-block;
          height: 60px;
          width: 60px;
          background-image: url('~@/assets/img/icon2.png');
          background-repeat: repeat;
          background-position: center center;
          background-size: cover;
        }
        .icon3{
          display: inline-block;
          height: 60px;
          width: 60px;
          background-image: url('~@/assets/img/icon3.png');
          background-repeat: repeat;
          background-position: center center;
          background-size: cover;
        }
        .icon4{
          display: inline-block;
          height: 60px;
          width: 60px;
          background-image: url('~@/assets/img/icon4.png');
          background-repeat: repeat;
          background-position: center center;
          background-size: cover;
        }
        .menuName{
          display: block;
          text-align: center;
        }
      }
    }
  }
</style>