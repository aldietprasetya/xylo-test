<template>
  <b-container class="content">
    <div class="content-wrapper">

      <slick class="content-wrapper__slide" ref="slick" :options="slickOptions">
        <a class="content-wrapper__slide-item" v-for="dt,i in dataSlider" :key="i" :href="dt.link">
          <img :src="dt.img">
          <div class="content-wrapper__slide-thumb">
            <span>NEW EPISODE</span>
          </div>
          <div class="content-wrapper__slide-speak">
            <span><img src="@/assets/images/logo-icon/speaker.svg"> Listen Now</span>
          </div>
          <div class="content-wrapper__slide-item_content">
            <h2>{{dt.title}}</h2>
            <p>
              {{dt.text}}
            </p>
            <p>Show Notes</p>
          </div>
        </a>
      </slick>

      <b-row class="content-wrapper__links">
        <b-col sm="4" class="content-wrapper__links-blocks" v-for="(dt,i) in dataLink" :key="i">
          <a href="#" class="content-wrapper__links-content">
            <div  class="content-wrapper__links-icons">
              <span class="content-wrapper__links-icon"
                :class="{'content-wrapper__links-icon_trending' : dt.imgType == 'trending',
                'content-wrapper__links-icon_release' : dt.imgType == 'release',
                'content-wrapper__links-icon_archieve' : dt.imgType == 'archieve'}"
              >
              </span>
            </div>
            <div class="content-wrapper__links-title">
              {{ dt.title }}
            </div>
            <div class="content-wrapper__links-text">
              {{ dt.text }}
            </div>
          </a>
        </b-col>
      </b-row>
    </div>

  </b-container>
</template>

<script>
import Slick from 'vue-slick';
export default {
  name: 'ContentComponent',
  components: { Slick },
  data() {
    return {
      dataLink: [
        {
          title: 'Trending Now',
          text: 'Find the interviews and articles that are trending now.',
          imgType: 'trending',
          link: 'https://www.danielscrivner.com/popular'
        },
        {
          title: 'New Releases',
          text: 'Catch up on all of the latest interviews and articles.',
          imgType: 'release',
          link: 'https://www.danielscrivner.com/latest'
        },
        {
          title: 'The Archieve',
          text: 'Explore the archives by browsing categories and tags.',
          imgType: 'archieve',
          link: 'https://www.danielscrivner.com/topics-and-tags'
        },
      ],
      dataSlider: [
        {
          title: '#111 – 20 Minute Playbook: Illia Polosukhin of NEAR Protocol and Unchain Fund',
          text: "In Episode #111, we deconstruct Illia Polosukhin's peak performance playbook—from his favorite book to the tiny habit that's had the biggest impact on his life. Illia is the co-founder of NEAR Protocol and Unchain Fund.",
          link: 'https://www.danielscrivner.com/notes/illia-polosukhin-playbook',
          img: require('@/assets/images/section3-img/Illia-Polosukhin_Thumbnail.jpg')
        },
        {
          title: '#110 Payload – Building a Media Brand to Cover the Business and Policy of Space | Mo Islam, Co-Founder',
          text: 'In Episode #110, we explore building a media brand to cover the business and policy of space. We’re joined by Mo Islam, Payload’s Co-Founder, who talks with us about becoming the number one resource for space industry news.',
          link: 'https://www.danielscrivner.com/notes/payload-mo-islam',
          img: require('@/assets/images/section3-img/Mo-Islam_Thumbnail.jpg')
        },
        {
          title: '20 Minute Playbook: Alex Simon – Co-Founder and CEO of Elude',
          text: 'Alex Simon is CEO and Co-Founder of Elude, a travel app that allows users to discover new destinations based on timing and budget. In this episode, Alex and Daniel discuss mentors, favorite books, and daily meditation.',
          link: 'https://www.danielscrivner.com/notes/alex-simon-elude-playbook-show-notes',
          img: require('@/assets/images/section3-img/Alex-Simon_Thumbnail.jpg')
        },
        {
          title: '20 Minute Playbook: Howie Schwab – Lead Portfolio Manager for Emerging Markets Growth at Driehaus Capital',
          text: 'Howie Schwab is Lead Portfolio Manager for Emerging Markets Growth at Driehaus Capital. In this episode, Howie and Daniel discuss regime shifts in the market and obsessing over failures.',
          link: 'https://www.danielscrivner.com/notes/howie-schwab-driehaus-capital-playbook-show-notes',
          img: require('@/assets/images/section3-img/Howie-Schwab_Thumbnail.jpg')
        },

      ],
      slickOptions: {
        //options can be used from the plugin documentation
        slidesToShow: 3,
        autoplay: true,
        autoplaySpeed: 8000,
        infinite: true,
        accessibility: true,
        adaptiveHeight: false,
        arrows: true,
        dots: true,
        draggable: true,
        edgeFriction: 0.30,
        swipe: true,
        mobileFirst: true,
      }
    }
  },
  methods: {
    next() {
      this.$refs.slick.next()
    },
    prev() {
      this.$refs.slick.prev()
    },
    reInit() {
      // Helpful if you have to deal with v-for to update dynamic lists
      this.$refs.slick.reSlick()
    }

  }
}
</script>
