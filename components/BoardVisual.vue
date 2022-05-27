<template>
  <div>
    <b-carousel
      id="carousel-fade"
      v-model="slide"
      :interval="0"
      controls
      indicators
      background="#ababab"
      img-width="1920"
      img-height="600"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-link to="/"><b-carousel-slide caption="자유 게시판" :img-src="require('../static/mainVisual1.png')" ></b-carousel-slide></b-link>
      <b-link to="/gallery"><b-carousel-slide caption="갤러리" text="흘러가버린 추억을 이곳에서 확인하세요." :img-src="require('../static/mainVisual2.png')" ></b-carousel-slide></b-link>
      <b-link to="/boardlist"><b-carousel-slide caption="공지사항/자료실" text="공지사항을 확인하세요." :img-src="require('../static/mainVisual3.png')" ></b-carousel-slide></b-link>
      <b-link to="/calvue"><b-carousel-slide caption="달력" text="달력으로 일정을 확인하세요" :img-src="require('../static/mainVisual4.png')" ></b-carousel-slide></b-link>
      <b-link to="/login"><b-carousel-slide caption="로그인" :img-src="require('../static/mainVisual5.png')" ></b-carousel-slide></b-link>
    </b-carousel>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>

<style>
.sr-only{position: absolute; left: -9999px; opacity: 0; }
</style>