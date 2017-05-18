<template>
	<a href="javascript:void(0);" id="goTop"
		v-on:click="goTop">
		<img src="../assets/img/go_top.png" alt="">
	</a>
</template>
<script>
  export default {
    name: 'gotop',
    methods: {
      goTop () {
        window.scrollTo(0, 0)
      }
    }
  }
</script>
<style>
#goTop {
	position: fixed;
	right: 5%;
	bottom: 10%;
	width: 50px;
	height: 50px;
}
</style>
