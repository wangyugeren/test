<template>
  <swiper :options="swiperOption">
    <swiper-slide v-for="(slide,index) in swiperSlides">
      <img v-bind:src="slide">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOption: {
          autoplay: 3500,
          setWrapperSize :true,
          pagination : '.swiper-pagination',
          paginationClickable :true,
          mousewheelControl : true,
          observeParents:true,
        },
        swiperSlides: [require("../assets/img/1.jpg"),require("../assets/img/2.jpg"),require("../assets/img/1.jpg"),require("../assets/img/2.jpg")]
      }
    },
    mounted() {
      // setInterval(() => {
      //   console.log('simulate async data')
      //   let swiperSlides = this.swiperSlides
      //   if (swiperSlides.length < 10) swiperSlides.push(swiperSlides.length + 1)
      // }, 3000)
    }
  }
</script>