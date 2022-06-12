<template>
  <b-container class="header">
    <b-navbar class="header__bottom-bar">
      <b-link class="header__menus" href="https://www.danielscrivner.com/outliers/episodes-and-guests">Podcast</b-link>
      <b-link class="header__menus" href="https://www.danielscrivner.com/newsletter">Newsletter</b-link>
      <b-link class="header__menus" href="https://www.danielscrivner.com/topics-and-tags">Topics & Tags</b-link>
      <div class="header__menus header__menus_dropdown" @mouseover="onOver" @mouseleave="onLeave">
        <b-nav-item-dropdown center class="header__menus-dropdown" ref="dropdown" text="More">
          <b-dropdown-item href="https://www.danielscrivner.com/about">About</b-dropdown-item>
          <b-dropdown-item href="https://www.danielscrivner.com/media">Newsroom</b-dropdown-item>
          <b-dropdown-item href="https://www.danielscrivner.com/contact">Contact</b-dropdown-item>
        </b-nav-item-dropdown>
      </div>
    </b-navbar>
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
