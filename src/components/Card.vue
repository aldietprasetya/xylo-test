<template>
  <b-container class="cards">
    <div class="cards__content">
      <div class="cards__content-title">
        {{ data.title }}
      </div>
      <div class="cards__content-subTitle">
        {{ data.subTitle }}
      </div>
      <div class="cards__content-text">
        {{ data.text }}
      </div>
      <b-button class="cards__content-button" :href="data.btnUrl">
        {{ data.btn }}
      </b-button>
    </div>
    <div class="cards__img-array">
      <div class="cards__img-block" v-rellax="{speed: dt.speed}" v-for="dt in data.img" :key="dt.id">
        <img :src="item.src" v-for="(item,i) in dt.list" :key="i">
      </div>
    </div>
  </b-container>
</template>

<script>
export default {
  name: 'BillboardComponent',
  props: {
    data: Object,
  },
  data() {
    return {

    }
  },
  mounted() {

  }
}
</script>
