<template>
  <div class="box">
    <textarea :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" class="textarea"
      placeholder="Write something for the StarCrew..." rows="3"></textarea>

    <div class="actions">
      <button @click="$emit('submit')" class="post-btn">Post</button>
    </div>

  </div>
</template>

<script setup>
const props = defineProps({
  modelValue: String
});
</script>

<style lang="scss" scoped>
.box {
  background: white;
  padding: 16px;
  border-radius: 18px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
  margin-bottom: 24px;
}

.textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 14px;
  resize: none;
  font-size: 14px;
}

.actions {
  display: flex;
  justify-content: flex-end;
  margin-top: 12px;
}

.post-btn {
  padding: 8px 16px;
  background: #2563eb;
  color: white;
  border-radius: 12px;
  font-weight: 500;
  cursor: pointer;
  border: none;
}
</style>
