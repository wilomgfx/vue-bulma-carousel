<template>
    <div>
        <section class="section">
          <div class="container">
            <vue-carousel :carousel-items="images" accent-color="is-info"></vue-carousel>
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
          title : 'The best image1',
          src : './src/assets/images/sports.1.jpg',
          desc : 'Laboris ullamco nostrud qui consectetur aute eiusmod irure aliquip veniam aliquip ut officia laboris amet. Consequat id excepteur mollit dolor fugiat labore. Commodo nulla minim eu commodo reprehenderit veniam eu aliqua aute cillum proident nostrud veniam. Anim voluptate nulla adipisicing in ullamco irure. Velit nostrud ad in duis ex minim nulla cupidatat duis esse nostrud ex ad exercitation. Duis ut do laborum commodo Lorem sunt aliqua labore ex occaecat aliqua nulla id.',
          other : ``
        },
        {
          title : 'The best image2',
          src : './src/assets/images/sports.2.jpg',
          desc : 'Non fugiat veniam ipsum Lorem anim sit culpa Lorem. Tempor culpa enim adipisicing nostrud exercitation cillum ex dolore dolor mollit irure enim velit commodo. Labore veniam esse incididunt consequat voluptate esse veniam deserunt excepteur. Lorem labore aute labore voluptate. Enim esse eu consectetur ex fugiat aliqua. Quis dolor amet nostrud ea.',
          other : ``
        },
        {
          title : 'The best image3',
          src : './src/assets/images/sports.3.jpg',
          desc : 'Ex in amet amet ea tempor nisi in commodo ullamco exercitation ea qui eiusmod.',
          other : ``
        },
        {
          title : 'The best image4',
          src : './src/assets/images/sports.5.jpg',
          desc : 'Sunt amet nisi non non excepteur amet occaecat nulla occaecat deserunt excepteur. Culpa occaecat nulla nulla ea ea. Non occaecat veniam elit in commodo ex esse ipsum occaecat cillum fugiat consequat. Aliquip laborum cupidatat elit in commodo commodo ea. Id esse labore adipisicing proident adipisicing anim sint exercitation nostrud velit. Veniam aliqua magna enim do.',
          other : ``
        },
      ]
    }
  }
}
</script>

<style>

</style>
