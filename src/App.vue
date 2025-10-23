<template>
  <ScrollingText
    v-for="text in scrollText"
    :children="text"
    :animation-duration="animationDuration"
    :ease="ease"
    :scroll-start="scrollStart"
    :scroll-end="scrollEnd"
    :stagger="stagger"
    :container-class-name="containerClassName"
    :text-class-name="textClassName"
    :scroll-container-ref="{ current: containerRef }"
    :key="rerenderKey"
  />
</template>

<script lang="ts">
import ScrollingText from './components/ScrollingText.vue'

export default {
  components: { ScrollingText },
  data() {
    return {
      scrollText: ['HELLO'],
      animationDuration: 5,
      ease: 'linear',
      scrollStart: '',
      scrollEnd: '',
      stagger: 0,
      containerClassName: '',
      textClassName: '',
      containerRef: null,
      rerenderKey: 0,
    }
  },
}
</script>
