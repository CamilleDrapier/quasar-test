<template>
  <input type="button" @click="toggle" value="toggle" />
  <div v-if="visible">
    <span>Visible</span>
    <div v-for="n in 10" :key="n">
      <KeepAliveComponent />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

import KeepAliveComponent from '../components/KeepAliveComponent.vue'

export default defineComponent({
  name: 'App',
  components: {
    KeepAliveComponent
  },
  data () {
    return {
      visible: false
    }
  },
  methods: {
    toggle () {
      this.visible = !this.visible
    }
  }
})
</script>
