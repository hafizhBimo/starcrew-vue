<template>
  <div class="profile-card">
    <!-- <img src="/avatar.png" class="avatar" /> -->

    <h2 class="name">Captain</h2>
    <p class="role">Founder of StarCrew 🚀</p>

    <div class="stats">
      <div><b>32</b><span>Posts</span></div>
      <div><b>512</b><span>Likes</span></div>
      <div><b>1400</b><span>Members</span></div>
    </div>

    <button class="edit-btn">Edit Profile</button>
  </div>
</template>

<style scoped>
.profile-card {
  background: white;
  padding: 24px;
  border-radius: 20px;
  box-shadow: 0 4px 14px rgba(0,0,0,0.08);
}

.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  display: block;
  margin: 0 auto 12px auto;
}

.name {
  text-align: center;
  font-size: 20px;
  font-weight: 700;
}

.role {
  text-align: center;
  font-size: 13px;
  color: #777;
  margin-bottom: 20px;
}

.stats {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
  text-align: center;
}

.stats span {
  display: block;
  color: #777;
  font-size: 12px;
}

.edit-btn {
  width: 100%;
  background: #3b82f6;
  color: white;
  padding: 10px;
  border-radius: 10px;
  font-weight: 600;
}
</style>
