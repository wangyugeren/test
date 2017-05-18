<template>
	<header id="headerNav">
	    <div class="logo">
	        <img src="../assets/img/logo.png" alt="">
	    </div>
	    <a href="#" class="search-bar">
	        <input type="text" placeholder="搜索商品名称">
	    </a>
	    <a href="#" class="login">登录</a>
	</header>
</template>
<script>
export default {
  name: 'header-nav'
}
</script>
<style>
  #headerNav {
      position: fixed;
      z-index: 10;
      width: 100%;
      max-width: 720px;
      top: 0;
      /*background: red;*/
      display: flex;
      height: 44px;
      line-height: 44px;
      font-size: 1.6rem;
  }
  #headerNav .logo img{
      width: 28px;
      height: 18px;
      margin-top: 13px;
  }

  #headerNav .search-bar {
      flex: 1;
  }
  #headerNav .logo, #headerNav .login {
      padding: 0 10px;
      color:#fff;
  }
  #headerNav .search-bar input {
      box-sizing: border-box;
      border-radius: 4px;
      width: 100%;
      border: none;
      padding: 6px 8px;
  }
</style>
