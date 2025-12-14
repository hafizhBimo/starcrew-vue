<template>
  <div class="bg-white rounded-2xl shadow p-4 mb-4">
    <div class="flex items-center mb-3">
      <img
        :src="post.avatar"
        class="w-10 h-10 rounded-full mr-3"
        alt="avatar"
      />
      <div>
        <p class="font-semibold">{{ post.username }}</p>
        <p class="text-xs text-gray-500">{{ post.time }}</p>
      </div>
    </div>

    <p class="text-gray-800 whitespace-pre-line">
      {{ post.message }}
    </p>
  </div>
</template>

<script setup>
defineProps({
  post: {
    type: Object,
    required: true
  }
});
</script>
