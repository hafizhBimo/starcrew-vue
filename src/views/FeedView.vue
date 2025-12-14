<template>
  <div class="page">
    <div class="main">
      <div class="container">
        <FeedHeader />

        <CreatePostBox />

        <PostFeed v-for="post in posts" :key="post.id" :post="post" />
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref } from "vue";
import CreatePostBox from "@/components/ui/CreatePostBox.vue";
import PostFeed from "@/components/ui/PostFeed.vue";
import FeedHeader from "@/components/ui/FeedHeader.vue";

const newPost = ref("");

function submitPost() {
  console.log(newPost.value);
}
</script>


<style>
body {
  font-family: Inter, sans-serif;
  margin: 0;
}

.page {
  min-height: 100vh;
  background-color: #f3f4f6;
  /* gray-100 */
  display: flex;
}

.main {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 24px 16px;
  overflow-y: auto;
}

.container {
  width: 100%;
  max-width: 640px;
  /* max-w-xl */
}
</style>
