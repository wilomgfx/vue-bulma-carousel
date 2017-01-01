<template>
    <div>
        <section class="section">
          <div class="container">
            <vue-carousel :carousel-items="images"></vue-carousel>
          </div>
      </section>
    </div>
</template>

<script>
import vueCarousel from './components/carousel.vue'
export default {
  name: 'app',
  components: {
    vueCarousel
  },
  data () {
    return {
      images : [
        {
          src : 'http://lorempixel.com/400/200/sports/1/',
          desc : 'Image1'
        },
        {
          src : 'http://lorempixel.com/400/200/sports/2/',
          desc : 'Image2'
        },
        {
          src : 'http://lorempixel.com/400/200/sports/3/',
          desc : 'Image3'
        },
        {
          src : 'http://lorempixel.com/400/200/sports/5/',
          desc : 'Image4'
        },
      ]
    }
  }
}
</script>

<style>

</style>
