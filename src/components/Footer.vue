<template>
  <b-container class="footer">
    <b-row class="footer-wrapper">
      <b-col sm="5" class="footer-wrapper__left-content">
        <p class="footer-wrapper__desc">
          Daniel Scrivner is an entreprenuer and investor focused on building enduring companies and breakthrough products.
        </p>
        <a class="footer-wrapper__link" href="#">
          See what he’s working on now
        </a>
        <a class="footer-wrapper__img" href="#"></a>

      </b-col>
      <b-col sm="7" class="footer-wrapper__right-content">
        <b-row class="footer-wrapper__link">
          <b-col sm="3" v-for="(val, id) in menuList" :key="id">
            <p>{{val.title}}</p>
            <a v-for="(dt, i) in val.menu" :key="i" :href="dt.link">{{dt.text}}</a>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row align-h="between" class="footer-base">
      <b-col cols="6" class="footer-base__copyright">Copyright © 2020 Daniel Scrivner. All rights reserved.</b-col>
      <b-col cols="4" class="text-right footer-base__menus">
        <b-link href="https://www.danielscrivner.com/legal/privacy-policy">Privacy & Terms</b-link>
        <b-link href="https://www.danielscrivner.com/legal/disclosures">Disclosures</b-link>
        <b-link href="https://www.danielscrivner.com/sitemap">Sitemap</b-link>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'FooterComponent',
  data() {
    return {
      menuList: [
        {id: 1, title: 'Explore', menu: [
          {
            text: 'Most Popular',
            link: "https://www.danielscrivner.com/popular"
          },
          {
            text: 'Most Recent',
            link: "https://www.danielscrivner.com/latest"
          },
          {
            text: 'Topics & Tags',
            link: "https://www.danielscrivner.com/topics-and-tags"
          },
          {
            text: 'Friday Five',
            link: "https://www.danielscrivner.com/friday-five"
          },
        ]},
        {id: 2, title: 'Outliers', menu: [
          {
            text: 'Episodes',
            link: "https://www.danielscrivner.com/outliers/episodes-and-guests"
          },
          {
            text: 'Subscirbe Now',
            link: "https://www.danielscrivner.com/outliers/where-to-listen"
          },
          {
            text: 'About the Show',
            link: "https://www.danielscrivner.com/outliers/about-the-show"
          },
          {
            text: 'Sponsors',
            link: "https://www.danielscrivner.com/outliers/sponsorships-and-advertising"
          },
        ]},
        {id: 3, title: 'Articles', menu: [
          {
            text: 'Show Notes',
            link: "https://www.danielscrivner.com/topic/show-notes"
          },
          {
            text: 'Subscirbe Now',
            link: "https://www.danielscrivner.com/topic/transcripts"
          },
          {
            text: 'Essays',
            link: "https://www.danielscrivner.com/topic/show-notes"
          },
          {
            text: 'Snippets',
            link: "https://www.danielscrivner.com/topic/snippets"
          },
        ]},
        {id: 4, title: 'More', menu: [
          {
            text: 'About Daniel',
            link: "https://www.danielscrivner.com/about"
          },
          {
            text: 'Business Card',
            link: "https://www.danielscrivner.com/card"
          },
          {
            text: 'Newsroom',
            link: "https://www.danielscrivner.com/media"
          },
          {
            text: 'Contact',
            link: "https://www.danielscrivner.com/contact"
          },
        ]},
      ],
    }
  },
}
</script>
