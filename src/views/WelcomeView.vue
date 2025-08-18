<template>
    <div class="welcome-screen">
        <h1 class="welcome-text">Welcome Starcrew!</h1>
        <div class="button-group">
            <RouterLink to="/register">
                <PixelButton bg-color="#ffd6a5" shadow-color="black" label="Register" />
            </RouterLink>
            <RouterLink to="/login">
                <PixelButton bg-color="#caffbf" shadow-color="black" label="Login" />
            </RouterLink>
        </div>
    </div>
</template>

<script setup>
import PixelButton from '@/components/ui/PixelButton.vue';
import { RouterLink } from 'vue-router';
</script>

<style lang="scss" scoped>
.welcome-screen {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex: 1;
    background-color: #84B6F4;
}

.welcome-text {
    font-size: 24px;
    color: #000;
    text-align: center;
    background: white;
    padding: 24px 32px;
    display: inline-block;
    position: relative;
    border: 4px solid #000;
    box-shadow: 6px 6px 0 black;
    margin-bottom: 32px;
    margin-left: 12px;
    margin-right: 12px;

    // Pixel speech bubble arrow
    &::after {
        content: "";
        position: absolute;
        bottom: -12px;
        left: 40%;
        width: 0;
        height: 0;
        border-left: 12px solid transparent;
        border-right: 12px solid transparent;
        border-top: 12px solid white;
        filter: drop-shadow(2px 2px 0 #000);
    }
}

.button-group {
    display: flex;
    gap: 16px;
    margin: 32px
}

// Import retro font
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
</style>
