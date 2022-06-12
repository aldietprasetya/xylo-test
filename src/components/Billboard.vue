<template>
  <b-container class="billboard">
    <b-row class="billboard-wrapper" cols-sm="2" cols-md="4" cols-lg="5">
      <b-col class="billboard-wrapper__column" v-for="(dt,i) in imgList" :key="i">
        <img class="billboard-wrapper__img" :src="dt.src">
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'BillboardComponent',
  data() {
    return {
      imgList: [
        {
          src:require('@/assets/images/section2-logo/logo-billboard.svg')
        },
        {
          src:require('@/assets/images/section2-logo/logo-nytimes.svg')
        },
        {
          src:require('@/assets/images/section2-logo/logo-bloomberg.svg')
        },
        {
          src:require('@/assets/images/section2-logo/logo-washpost.svg')
        },
        {
          src:require('@/assets/images/section2-logo/logo-espn.svg')
        },
      ]
    }
  },
  mounted() {

  }
}
</script>
