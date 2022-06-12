<template>
  <b-container class="subscribe">
    <div class="subscribe-wrapper">
      <b-row class="subscribe-wrapper__cards" cols-sm="1" cols-md="1" cols-lg="2">
        <Card v-for="(dt,i) in cards" :key="i" :data='dt'></Card>
      </b-row>
      <div class="subscribe-wrapper__subscribe">
        <h1 class="subscribe-wrapper__subscribe-title">GET THE WEEKLY SUMMARY</h1>
        <p class="subscribe-wrapper__subscribe-text">Join 7,500+ including Fortune 500 CEOs,
          championship coaches, and bestselling authors
          who get my free weekly summary.
        </p>
        <b-input-group class="subscribe-wrapper__subscribe-input">
          <b-form-input placeholder="Enter your email..."></b-form-input>

          <b-input-group-append>
            <b-button variant="outline-secondary">Try It</b-button>
          </b-input-group-append>
        </b-input-group>
        <p class="subscribe-wrapper__subscribe-policy">
          By subscribing, you agree to our <a href="https://www.danielscrivner.com/legal/privacy-policy">privacy policy</a>.
        </p>
      </div>
    </div>
  </b-container>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
  name: 'BillboardComponent',
  components: {
    Card,
  },
  data() {
    return {
      cards: [
        {
          title:'LISTEN NOW',
          subTitle:'Outliers Podcast',
          text:"Every week, I sit down with someone in the Top 1% of their field to decode what they've mastered and what they've learned along the way.",
          btn:'Explore Episodes',
          btnUrl:'https://www.danielscrivner.com/outliers/episodes-and-guests',
          img:[
            {
              id:1,
              list: [
                {src:require('@/assets/images/section4-img/block1/ds-home-1.jpg')},
                {src:require('@/assets/images/section4-img/block1/ds-home-4.jpg')},
              ],
              speed:-.1
            },
            {
              id:2,
              list: [
                {src:require('@/assets/images/section4-img/block2/ds-home-11.jpg')},
                {src:require('@/assets/images/section4-img/block2/ds-home-12.jpg')},
              ],
              speed:-.7
            },
            {
              id:3,
              list: [
                {src:require('@/assets/images/section4-img/block3/ds-home-2.jpg')},
                {src:require('@/assets/images/section4-img/block3/ds-home-3.jpg')},
              ],
              speed:-.1
            },
          ]
        },
        {
          title:'SUBSCRIBE NOW',
          subTitle:'Friday 5 Email',
          text:"Every Friday, I share five things I've been reading, using, and loving—including articles, biohacks, gadgets, and more.",
          btn:'Subscribe Now',
          btnUrl:'https://www.danielscrivner.com/friday-five',
          img:[
            {
              id:1,
              list: [
                {src:require('@/assets/images/section4-img/block4/ds-home-5.jpg')},
                {src:require('@/assets/images/section4-img/block4/ds-home-8.jpg')},
              ],
              speed:-.1
            },
            {
              id:2,
              list: [
                {src:require('@/assets/images/section4-img/block5/ds-home-9.jpg')},
                {src:require('@/assets/images/section4-img/block5/ds-home-10.jpg')},
              ],
              speed:-.7
            },
            {
              id:3,
              list: [
                {src:require('@/assets/images/section4-img/block6/ds-home-6.jpg')},
                {src:require('@/assets/images/section4-img/block6/ds-home-7.jpg')},
              ],
              speed:-.1
            },
          ]
        },
      ]
    }
  },
  mounted() {

  }
}
</script>
