<template>
  <div class="picture-component">
    <img
      :class="{
        mobile: getIsMobile,
        desktop: !getIsMobile
      }"
      :src="require(`@/${getOptimizedImage}`)"
      :alt="altText" />

  </div>
</template>
<script>
import isMobile from '@/utils/isMobile'

export default {
  name: 'Picture',
  props: {
    imgName: {
      type: String,
      required: true
    },
    altText: {
      type: String,
      required: true
    }
  },
  computed: {
    getIsMobile: function() {
      return isMobile()
    },
    
    getOptimizedImage: function () {
      return `assets/images/${isMobile() ? 'mobile' : 'desktop'}/${this.imgName}`
    }
  }
}
</script>

<style lang="scss" scoped>
.desktop {
  width: 100%;
}

.mobile {
  width: 100%;
}
</style>
