<template>
  <div>
    <keep-alive>
      <OtherComponent v-if="visible" />
    </keep-alive>
  </div>
</template>

<script>
import OtherComponent from './OtherComponent.vue'

export default {
  name: 'KeepAliveComponent',
  components: {
    OtherComponent
  },
  data () {
    return {
      visible: true
    }
  },
  mounted () {
    this.visible = false
  }
}
</script>
