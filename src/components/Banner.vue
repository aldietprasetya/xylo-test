<template>
  <b-container class="banner">
    <b-col sm="6" class="banner-wrapper__right-content banner-wrapper__right-content_mobile">
      <img v-rellax="{speed: -.8}" class="banner-wrapper__img" src="@/assets/images/section1-img/card-portrait-tiny.png">
    </b-col>
    <b-row class="banner-wrapper">
      <b-col sm="6" class="banner-wrapper__left-content">
        <h1>Timeless insights for business and life.</h1>
        <p>Every week, I sit down with someone in the Top 1% of their field
          — from NYT bestselling authors to Oscar winners —
          to decode what they've mastered. Listen as I uncover the tactics,
          routines, and habits that will propel you to the top of your field.
        </p>
        <b-row class="banner-wrapper__card-container">
          <b-col sm="12" class="banner-wrapper__cards">
            <b-button class="banner-wrapper__cards-button" href="#">
              <b-card class="banner-wrapper__cards-section" :img-src="require('@/assets/images/section1-img/Illia-Polosukhin_Thumbnail.jpg')" img-alt="Card image" img-left>
                <b-card-text>
                  <span class="">
                    Latest Episode
                  </span>
                  <span class="">
                    #111 – 20 Minute Playbook: Illia Polosukhin of NEAR Protocol and Unchain Fund
                  </span>
                </b-card-text>
              </b-card>
            </b-button>
          </b-col>
          <b-row class="banner-wrapper__card-container">
            <b-button class="banner-wrapper__cards-button banner-wrapper__cards-button_sec" href="#">Start Here</b-button>
            <b-button class="banner-wrapper__cards-button banner-wrapper__cards-button_sec" href="#">Listen to the Podcast</b-button>
          </b-row>
        </b-row>
      </b-col>
      <b-col sm="6" class="banner-wrapper__right-content banner-wrapper__right-content_desk">
        <img v-rellax="{speed: -.8}" class="banner-wrapper__img" src="@/assets/images/section1-img/card-portrait-tiny.png">
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'BannerComponent',
  data() {
    return {

    }
  },
  mounted() {

  }
}
</script>
