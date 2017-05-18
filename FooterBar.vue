<template>
    <footer id="footer">
		<ul>
			<li v-for="(item, index) in fooList"
          v-bind:class="['foo-icon-'+(index+1), {
              active: $route.path === item.path
            }]">
				<router-link v-bind:to="item.path">
					{{ item.text }}
				</router-link>
			</li>
		</ul>
	</footer>
</template>
<script>
export default {
  name: 'footerbar',
  data () {
    return {
      fooList: [{
        path: '/',
        text: '首页'
      },
      {
        path: '/category',
        text: '分类'
      },
      {
        path: '/cart',
        text: '购物车'
      },
      {
        path: '/user',
        text: '我的'
      }]
    }
  }
}
</script>
<style>
  #footer {
    height: 44px;
    margin-top: 10px;
  }
  #footer ul {
    position: fixed;
    left:0;
    bottom:0;
    width:100%;
    height: 44px;
    border-top:1px solid #d9d9d9;
    background-color: #fff;
      display: flex;
      font-size: 1.4rem;
  }
  #footer ul li {
    flex:1;
    text-align: center;
  }
  #footer ul li a {
    padding-top: 4px;
    padding-bottom: 2px;
    display: block;
    color:#333;
  }
  #footer ul li a:before {
    display: block;
    margin: 0 auto;
    content:"";
    width:20px;
    height: 20px;
    background: url(../assets/img/spr1.png) no-repeat;
    background-size: 20px 160px;
  }
  #footer ul .active a {
      color: #f66b01;
  }
  #footer ul .foo-icon-1 a:before {
    background-position: center -140px;
  }
  #footer ul .foo-icon-1.active a:before {
    background-position: center -120px;
  }

  #footer ul .foo-icon-2 a:before {
    background-position: center -59px;
  }
  #footer ul .foo-icon-2.active a:before {
    background-position: center -40px;
  }

  #footer ul .foo-icon-3 a:before {
    background-position: center -100px;
  }
  #footer ul .foo-icon-3.active a:before {
    background-position: center -80px;
  }

  #footer ul .foo-icon-4 a:before {
    background-position: center -20px;
  }
  #footer ul .foo-icon-4.active a:before {
    background-position: center 0;
  }
</style>
