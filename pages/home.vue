<template>
  <div>
    <div class="container">
    <AppNavBar />
    </div>
  <body>
    <div class="carousel">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=55"></b-carousel-slide>
    </b-carousel>
  </div>
</body>
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