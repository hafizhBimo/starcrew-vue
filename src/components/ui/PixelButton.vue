<template>
  <button
    class="pixel-btn"
    :style="{
      backgroundColor: bgColor,
      color: textColor,
      boxShadow: `${shadowOffset} ${shadowOffset} 0 ${shadowColor}`,
      padding: padding
    }"
  >
    <slot>{{ label }}</slot>
  </button>
</template>

<script setup>
const props = defineProps({
  label: { type: String, default: 'Themed Button' },
  bgColor: { type: String, default: '#fffecf' }, // Light yellow
  textColor: { type: String, default: '#000000' }, // Black text
  shadowColor: { type: String, default: '#d28bb3' }, // Purple shadow
  shadowOffset: { type: String, default: '6px' }, // Default shadow
  padding: { type: String, default: '12px 24px' } // ✅ Customizable padding
});
</script>

<style lang="scss" scoped>
.pixel-btn {
  font-family: 'Press Start 2P', cursive;
  font-size: 18px;
  cursor: pointer;
  border: 4px solid #000;
  position: relative;
  text-align: center;
  outline: none;
  user-select: none;

  // 8-bit animation
  transition: transform steps(2, end), box-shadow steps(2, end);

  &:hover {
    transform: translate(2px, 2px);
    box-shadow: 4px 4px 0 var(--shadow-color, #d28bb3);
  }

  &:active {
    transform: translate(4px, 4px);
    box-shadow: 2px 2px 0 var(--shadow-color, #d28bb3);
  }
}

// Import retro pixel font
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
</style>
