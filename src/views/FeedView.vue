<template>
  <div class="min-h-screen bg-gray-100 flex">

    <!-- Main Content -->
    <div class="flex-1 flex flex-col items-center py-6 px-4 overflow-y-auto">
      <div class="w-full max-w-xl">
        <!-- Header -->
        <header class="mb-6 flex items-center justify-between">
          <h1 class="text-2xl font-bold">StarCrew Feed</h1>
        </header>

        <!-- Create Post Box -->
        <div class="bg-white rounded-2xl shadow p-4 mb-6">
          <textarea
            v-model="newPost"
            placeholder="Write something for the StarCrew..."
            class="w-full p-3 border rounded-xl resize-none"
            rows="3"
          ></textarea>
          <div class="flex justify-end mt-3">
            <button @click="submitPost" class="px-4 py-2 bg-blue-600 text-white rounded-xl">
              Post
            </button>
          </div>
        </div>

        <!-- Posts Feed -->
        <div v-for="post in posts" :key="post.id" class="bg-white rounded-2xl shadow p-4 mb-4">
          <div class="flex items-center mb-3">
            <img :src="post.avatar" class="w-10 h-10 rounded-full mr-3" />
            <div>
              <p class="font-semibold">{{ post.username }}</p>
              <p class="text-xs text-gray-500">{{ post.time }}</p>
            </div>
          </div>
          <p class="text-gray-800 whitespace-pre-line">{{ post.message }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeedPage",
  data() {
    return {
      newPost: "",
      posts: [
        {
          id: 1,
          username: "StarFan01",
          avatar: "https://api.dicebear.com/8.x/bottts/svg?seed=Fan01",
          time: "Just now",
          message: "Welcome to the StarCrew feed! ✨🚀",
        },
      ],
    };
  },
  methods: {
    submitPost() {
      if (!this.newPost.trim()) return;
      this.posts.unshift({
        id: Date.now(),
        username: "You",
        avatar: "https://api.dicebear.com/8.x/bottts/svg?seed=You",
        time: "Just now",
        message: this.newPost,
      });
      this.newPost = "";
    },
  },
};
</script>

<style>
body {
  font-family: Inter, sans-serif;
}
</style>
