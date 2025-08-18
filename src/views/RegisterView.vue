<script setup lang="ts">
import PixelBox from '@/components/ui/PixelBox.vue';
import PixelInput from '@/components/ui/PixelInput.vue';
import PixelButton from '@/components/ui/PixelButton.vue';
import { ref } from 'vue';
import { RouterLink } from 'vue-router';
import router from '@/router';

const username = ref('');
const email = ref('');
const password = ref('');

const register = () => {
    // Handle registration logic here
};

const goBack = () => {
  router.back();
};
</script>

<template>
    <div class="register-screen">
        <PixelBox backgroundColor="white" borderColor="#000" shadowColor="#000" width="800px">
            <div class="header">
                <PixelButton class="back-button" @click="goBack" padding="0px 5px" shadow-color="black" bg-color="#FF4C4C"> X </PixelButton>
                <h1>Register</h1>
            </div>
            <form @submit.prevent="register">
                <PixelInput v-model="username" placeholder="Username" />
                <PixelInput v-model="email" type="email" placeholder="Email" />
                <PixelInput v-model="password" type="password" placeholder="Password" />
                <PixelButton bg-color="#ffd6a5" label="Register" shadow-color="black" />
            </form>
        </PixelBox>
        <p>Already have an account? <RouterLink class="login-link" to="/login">Login here</RouterLink>
        </p>
    </div>
</template>

<style scoped>
.register-screen {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex: 1;
    background-color: #84B6F4;
}

.pixel-input {
    margin-bottom: 16px;
}

.pixel-button {
    margin-top: 16px;
}

.header {
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 16px;
}

.login-link {
  font-family: 'Press Start 2P', cursive;
  font-size: 14px;
  text-decoration: none;
  color: #000;
  position: relative;
  font-weight: bold;

  &:hover {
    color: #0d18ec;
    padding: 4px 6px;
  }
}


</style>