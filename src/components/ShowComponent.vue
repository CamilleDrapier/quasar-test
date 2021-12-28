<template>
  <div>
    <OtherComponent v-show="visible" />
  </div>
</template>

<script>
import OtherComponent from './OtherComponent.vue'

export default {
  name: 'ShowComponent',
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
