<template>
  <input
    class="pixel-input"
    :placeholder="placeholder"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>

<script setup>
const props = defineProps({
  modelValue: {
    type: String,
    default: ''
  },
  placeholder: {
    type: String,
    default: 'Type here...'
  },
});

</script>

<style lang="scss" scoped>
.pixel-input {
  font-family: 'Press Start 2P', cursive;
  font-size: 16px;
  width: 100%;
  padding: 12px;
  background: #ffffff;
  color: #000;
  border: 4px solid #000;
  box-shadow:   4px 4px 0 #000;
  outline: none;

  transition: all 0.1s steps(2, end);

  &::placeholder {
    color: #888;
  }

  &:hover {
    border-color: #000;
    box-shadow:   4px 4px 0 #000;
  }

  &:focus {
    background-color: #fffefc;
    border-color: #000;
    box-shadow:   4px 4px 0 #000;
  }
}

// Import pixel font
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
</style>
