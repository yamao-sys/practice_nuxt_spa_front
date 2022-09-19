<template>
  <div class="container">
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item.title }}</li>
    </ul>
  </div>
</template>
<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'
import { DefaultLayoutItem } from '@/types/default_layout_item'

export default defineComponent({
  setup() {
    const clipped = ref(false)
    const drawer = ref(false)
    const fixed = ref(false)

    const items = ref<DefaultLayoutItem[]>([
      {
        icon: 'mdi-apps',
        title: 'Welcome',
        to: '/'
      },
      {
        icon: 'mdi-chart-bubble',
        title: 'Inspire',
        to: '/inspire'
      },
    ])

    const miniVariant = ref(false)
    const right = ref(false)
    const rightDrawer = ref(false)
    const title = ref('Vuetify.js')

    return {
      clipped,
      drawer,
      fixed,
      items,
      miniVariant,
      right,
      rightDrawer,
      title
    }
  }
})
</script>
