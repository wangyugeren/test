<template>
	<div>
			<todo v-bind:todolist="todo"></todo>
	  	<header-nav></header-nav>
	  	<swiper-banner></swiper-banner>
	    <div class="top-news">
	        <div class="news-logo">
	            <img src="../assets/img/news_logo.png" alt="">
	        </div>
	        <a href="#" class="news-title ellipsis">
	            <span>|</span>
	            出行新玩物，米家电动滑板车开箱
	        </a>
	    </div>
	    <div id="product">
	        <section>
	            <div class="head-product">
	                <a href="#">
	                    <img src="../assets/img/p1.jpg" alt="">
	                </a>
	            </div>
	            <ul class="product-list">
	                <li>
	                    <a href="">
	                        <div>
	                            <img src="../assets/img/p2.jpg" alt="">
	                        </div>
	                        <div class="tips">
	                            <h2 class="ellipsis">小米手环2</h2>
	                            <p class="sub-title ellipsis">OLED 显示屏，触摸操作</p>
	                            <p class="price">&yen; 149</p> 
	                        </div> 
	                    </a>
	                </li>
	                <li>
	                    <a href="">
	                        <div>
	                            <img src="../assets/img/p2.jpg" alt="">
	                        </div>
	                        <div class="tips">
	                            <h2 class="ellipsis">小米手环2</h2>
	                        <p class="sub-title ellipsis">OLED 显示屏，触摸操作</p>
	                        <p class="price">&yen; 149</p> 
	                        </div> 
	                    </a>
	                </li>
	                <li>
	                    <a href="">
	                        <div>
	                            <img src="../assets/img/p2.jpg" alt="">
	                        </div>
	                        <div class="tips">
	                            <h2 class="ellipsis">小米手环2</h2>
	                        <p class="sub-title ellipsis">OLED 显示屏，触摸操作</p>
	                        <p class="price">&yen; 149</p> 
	                        </div> 
	                    </a>
	                </li>
	                <li>
	                    <a href="">
	                        <div>
	                            <img src="../assets/img/p2.jpg" alt="">
	                        </div>
	                        <div class="tips">
	                            <h2 class="ellipsis">小米手环2</h2>
	                        <p class="sub-title ellipsis">OLED 显示屏，触摸操作</p>
	                        <p class="price">&yen; 149</p> 
	                        </div> 
	                    </a>
	                </li>
	            </ul>
	        </section>
	    </div>
	    
	    <go-top></go-top>
	</div>
</template>
<script>
import HeaderNav from './HeaderNav'
import SwiperBanner from './SwiperBanner'
import GoTop from './GoTop'
import Todo from './Todo'
export default {
  name: 'index',
  components: {
  	'todo': Todo,
    'header-nav': HeaderNav,
    'swiper-banner': SwiperBanner,
    'go-top': GoTop
  },
  data () {
  	return {
  		todo: ["a","b","c"]
  	}
  }
}
</script>
<style>
	
</style>
