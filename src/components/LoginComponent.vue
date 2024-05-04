<template>
  <div>
    <input v-model="username" placeholder="Username" />
    <input v-model="password" placeholder="Password" type="password" />
    <button @click="login">Login</button>
  </div>
</template>
<script setup lang="ts">
import { ref, onMounted } from 'vue'
import axios from 'axios'
const username = ref('')
const password = ref('')
async function login() {
  try {
    await axios.post(
      'http://localhost:8081/login',
      { username: username.value, password: password.value },
      { withCredentials: true }
    )
    console.log('Login successful')
  } catch (error) {
    console.error('Login failed', error)
  }
}

onMounted(() => {
  document.title = 'Login Page'
})
</script>
