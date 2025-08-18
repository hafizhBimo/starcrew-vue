<template>
  <footer class="pixel-footer">
    <p class="footer-text">© 2024 StarCrew. All rights reserved.</p>
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
  </footer>
</template>


<script setup>
// No logic needed for now, purely presentational
</script>

<style scoped lang="scss">
.pixel-footer {
  display: flex;
  justify-content: center; /* Centers content */
  align-items: center;
  position: relative; /* So we can absolutely position icons */
  padding: 16px;
  // background-color: #000;
  // color: #fff;
  // border-top: 4px solid #fff;
  // box-shadow: 0 -4px 0 #000;
  font-family: 'Press Start 2P', cursive;
  font-size: 12px;
}

.footer-text {
  text-align: center;
}

.social-links {
  position: absolute;
  right: 16px; /* Push icons to the right */
  display: flex;
  gap: 20px;

  img {
    width: 40px;  /* Bigger size */
    height: 40px;
    image-rendering: pixelated;
    cursor: pointer;

    &:hover {
      transform: scale(1.3);
    }
  }
}
</style>


