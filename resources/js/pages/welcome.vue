<template>
  <div>
    <div class="text-center">
      <div class="text-6xl font-thin text-gray-500 mt-16 mb-8" dusk="title">
        {{ title }}
      </div>

      <div>
        <p class="font-bold">by Marlon Ocsan</p>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  layout: 'default',

  metaInfo () {
    return { title: this.$t('home') }
  },

  data: () => ({
    title: window.config.appName
  }),

  computed: mapGetters({
    authenticated: 'auth/check'
  })
}
</script>

<style scoped>
.top-right {
  position: absolute;
  right: 10px;
  top: 18px;
}

</style>
