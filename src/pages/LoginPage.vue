<template>
  <div class="login-page">
    <video autoplay muted loop id="background-video">
      <source src="/src/assets/mylivewallpapers.com-Rick-N-Morty-Adventures.mp4" type="video/mp4">
    </video>
    <div class="login-form">
      <q-card>
        <q-card-section>
            <q-input v-model="username" label="Username" outlined dense/>
          </q-card-section>
          <q-card-actions align="center">
            <q-btn label="Login" type="submit" color="primary" unelevated/>
        </q-card-actions>
      </q-card>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoginPage',
  data() {
    return {
      username: '',
    };
  },
});
</script>

<style lang="scss">
.login-page {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

#background-video {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transform: translate(-50%, -50%);
  z-index: -1;
}

.login-form {
  position: relative;
  z-index: 1;
  width: 90%;
  max-width: 400px;
  padding: 20px;
  box-sizing: border-box;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.q-card {
  width: 100%;
  background: none;
  box-shadow: none;
}
</style>
