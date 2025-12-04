<template>
  <footer class="pixel-footer">
    <div class="social-links">
      <a href="https://www.youtube.com/@StarmanPlay" target="_blank" rel="noopener noreferrer">
        <img src="@/assets/logo/youtubelogo.png" alt="YouTube" />
      </a>
      <a href="https://x.com/starmanplay" target="_blank" rel="noopener noreferrer">
        <img src="@/assets/logo/twitterlogo.png" alt="Twitter" />
      </a>
      <a href="https://discord.gg/jg6bxrttcu" target="_blank" rel="noopener noreferrer">
        <img src="@/assets/logo/discordlogo.png" alt="Discord" />
      </a>
    </div>
    <p class="footer-text">© 2024 StarCrew. All rights reserved.</p>
  </footer>
</template>

<script setup>
// No logic needed
</script>

<style scoped lang="scss">
.pixel-footer {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  padding: 16px;
  font-family: 'Press Start 2P', cursive;
  font-size: 12px;

  // Default layout (desktop)
  flex-direction: row;
}

.footer-text {
  text-align: center;
}

.social-links {
  position: absolute;
  right: 16px;
  display: flex;
  gap: 20px;

  img {
    width: 40px;
    height: 40px;
    image-rendering: pixelated;
    cursor: pointer;
    transition: transform 0.2s ease;

    &:hover {
      transform: scale(1.3);
    }
  }
}

@media (max-width: 600px) {
  .pixel-footer {
    flex-direction: column;
    text-align: center;
    position: relative;
    padding: 20px;
  }

  .social-links {
    position: static;
    margin-bottom: 10px;
    justify-content: center;
  }
}
</style>
