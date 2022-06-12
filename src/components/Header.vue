<template>
  <b-container class="header header_fixed">
    <b-navbar class="header__top-bar" toggleable>

      <b-button class="header__button header__button_1 header__button-icon" v-b-modal.modal-1 href="#">
        <b-icon icon="search"></b-icon>
      </b-button>

      <a class="header__img" href="#"></a>

      <b-navbar-toggle class="header__toogle" target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
          <b-icon v-else icon="chevron-bar-down"></b-icon>
        </template>
      </b-navbar-toggle>
      <b-button class="header__button header__button_subscribe" href="#">Subscribe</b-button>
      <b-button class="header__button header__button_t header__button-icon" v-b-modal.modal-1 href="#">
        <b-icon icon="search"></b-icon>
      </b-button>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="https://www.danielscrivner.com/outliers/episodes-and-guests">Podcast</b-nav-item>
          <b-nav-item href="https://www.danielscrivner.com/newsletter">Newsletter</b-nav-item>
          <b-nav-item href="https://www.danielscrivner.com/topics-and-tags">Topics & Tags</b-nav-item>
          <b-nav-item href="https://www.danielscrivner.com/about">About</b-nav-item>
          <b-nav-item href="https://www.danielscrivner.com/media">Newsroom</b-nav-item>
          <b-nav-item href="https://www.danielscrivner.com/contact">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <b-modal class="header__modal" id="modal-1" title="BootstrapVue">
      <template #modal-title>
        Quickly find episodes, articles, and pages across the website.
      </template>
      <div class="modal-middle">
        <input type="text" placeholder="Search...">
        <b-button block>Search</b-button>
      </div>
      <div class="modal-bottom">
        <a class="modal-bottom__link">
          <span>
            <img src="@/assets/images/section3-icon/popular-white.svg">
          </span>
          Popular
        </a>
        <a class="modal-bottom__link">
          <span>
            <img src="@/assets/images/section3-icon/latest-posts-white.svg">
          </span>
          Recent
        </a>
        <a class="modal-bottom__link">
          <span>
            <img src="@/assets/images/section3-icon/topics-and-tags-white.svg">
          </span>

          Browse All
        </a>
      </div>
    </b-modal>
  </b-container>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
    }
  },
  methods: {
    onOver() {
      this.$refs.dropdown.visible = true;
    },
    onLeave() {
      this.$refs.dropdown.visible = false;
    }
  }
}
</script>
