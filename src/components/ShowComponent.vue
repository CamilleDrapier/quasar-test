<template>
  <img v-show="visible" loading="lazy" src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" />
</template>

<script>
export default {
  name: 'ShowComponent',
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
