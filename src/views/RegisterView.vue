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
        <PixelBox 
          class="register-box"
          backgroundColor="white"
          borderColor="#000"
          shadowColor="#000"
          width="800px"
        >
            <div class="header">
                <PixelButton class="back-button" @click="goBack" padding="0px 5px" shadow-color="black" bg-color="#FF4C4C">
                  X
                </PixelButton>
                <h1>Register</h1>
            </div>
            <form @submit.prevent="register">
                <PixelInput v-model="username" placeholder="Username" />
                <PixelInput v-model="email" type="email" placeholder="Email" />
                <PixelInput v-model="password" type="password" placeholder="Password" />
                <PixelButton bg-color="#ffd6a5" label="Register" shadow-color="black" />
            </form>
        </PixelBox>
        <p class="login-text">
          Already have an account? 
          <RouterLink class="login-link" to="/login">Login here</RouterLink>
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
    padding: 20px;
    min-height: 100vh;
    box-sizing: border-box;
}

.register-box {
    width: 100%;
    max-width: 800px; /* Prevents it from being too large */
    padding: 20px;
    box-sizing: border-box;
}

.pixel-input {
    margin-bottom: 16px;
    width: 100%;
}

.pixel-button {
    margin-top: 16px;
    width: 100%; /* Full width for better UX on mobile */
}

.header {
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;

    h1 {
        font-size: 24px;
    }
}

.login-text {
    text-align: center;
    margin-top: 16px;
    font-size: 14px;
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

/* ✅ Responsive Adjustments */
@media (max-width: 768px) {
    .register-box {
        max-width: 100%;
        padding: 16px;
    }

    .header h1 {
        font-size: 20px;
    }

    .pixel-button {
        font-size: 12px;
    }

    .login-link {
        font-size: 12px;
    }
}

@media (max-width: 480px) {
    .header {
        flex-direction: column;
        gap: 12px;
        text-align: center;
    }

    .header h1 {
        font-size: 18px;
    }

    .pixel-input input {
        font-size: 14px;
    }
}
</style>
