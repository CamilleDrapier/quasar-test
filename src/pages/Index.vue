<template>
  <input type="button" @click="toggle" value="toggle" />
  <div v-if="visible">
    <span>Visible</span>
    <div v-for="n in 10" :key="n">
      <ShowComponent />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

import ShowComponent from '../components/ShowComponent.vue'

export default defineComponent({
  name: 'App',
  components: {
    ShowComponent
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
