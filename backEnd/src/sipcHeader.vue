<template>
  <div class="sipc-header" id="sipcHeader">
      <div class="header-logo">
          <img src="assets/sipclogo.png" alt="sipclogo" />
          <span v-text="headerTitle" class="logo-text"></span>
          <a href="javascript:void(0)" class="header-logout"></a>
          <span class="header-user">{{headerUser}}</span>
      </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        headerTitle: '学生创新实践中心后台',
        headerUser:"AdminUser"
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
    margin: 0;
    padding: 0;

}
  .sipc-header {
      box-shadow: 0 0 5px #888;
      width: 100%;
      position: fixed;
      top: 0;
      left: 0;
      height: 45px;
      min-width: 1002px;
  }
  .header-logo {
      height: 45px;
      line-height: 45px;
  }

  .header-logo img {
      height: 45px;
      margin-left: 50px;
      float: left;
  }
  .logo-text{
      float: left;
      height: 45px;
      color: black;
      font-weight: bold;
      margin-left: 25px;
  }
  .header-logout {
      float: right;
      margin-right: 50px;
      background:url("assets/logout.png") no-repeat center center;
      background-size: 25px 25px;
      height: 45px;
      width: 45px;
  }
  .header-logout:hover {
      animation: logout 1.5s linear infinite;
  }
  .header-user {
      float: right;
      margin-right: 25px;
  }
  @keyframes logout {
      0%{transform: translate3d(0,0,0)}
      25%{transform: translate3d(-3px,0,0)}
      50%{transform: translate3d(0,0,0)}
      75%{transform: translate3d(3px,0,0)}
      100%{transform: translate3d(0,0,0)}
  }
</style>
