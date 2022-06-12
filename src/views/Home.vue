<template>
  <div>
    <Banner></Banner>
    <Billboard></Billboard>
    <Content></Content>
    <Subscribe></Subscribe>
  </div>
</template>

<script>
import Banner from '@/components/Banner.vue'
import Billboard from '@/components/Billboard.vue'
import Content from '@/components/Content.vue'
import Subscribe from '@/components/Subscribe.vue'
export default {
  name: 'HomeViews',
  components: {
    Banner,
    Billboard,
    Subscribe,
    Content,
  },
  data() {
    return {
    }
  },
  methods: {

  }
}
</script>
