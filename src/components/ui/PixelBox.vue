<template>
  <div class="pixel-box" :style="boxStyle">
    <slot></slot>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  backgroundColor: { type: String, default: '#fff' },
  borderColor: { type: String, default: '#000' },
  shadowColor: { type: String, default: '#000' },
  width: { type: String, default: 'auto' } // NEW
})

const boxStyle = computed(() => ({
  backgroundColor: props.backgroundColor,
  border: `4px solid ${props.borderColor}`,
  boxShadow: `6px 6px 0 ${props.shadowColor}`,
  width: props.width
}))
</script>


<style scoped>
.pixel-box {
  display: inline-block;
  padding: 12px 16px;
  position: relative;
  margin: 12px;
  font-family: 'Press Start 2P', cursive;
}
</style>
