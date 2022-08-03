<template>
  <form @submit.prevent="login">
    <h2>Login Form</h2>
    <div class="email">
      <label>Email</label>
      <input type="email" v-model="email" autofocus required>
    </div>
    <div class="passwordInput">
      <label>Password</label>
      <input type="password" v-model="password" required>
    </div>
    <button type="submit">Login</button>
  </form>

 <p>
  this is what v-model does:
 </p>
  <p>
    {{ email }}
  </p>
  <p>
    this is what v-model does:
  </p>
  <p>
    {{ password }}
  </p>

</template>

<script setup lang="ts">

import {ref} from "vue";

const email = ref("");
const password = ref("");

function login() {
  console.log("this is my email, ", email.value)
  console.log("this is my password, ", password.value)
}

</script>

<style scoped>


form {
  color: whitesmoke;
  padding: 2rem 3rem;
  border-radius: 8px;
  background: lightblue;
  max-width: 250px;
}

div {
  margin-bottom: 1rem;
}

input {
  outline: none;
  border: none;
  border-radius: 5px;
  padding: 0.3rem;
}

.email {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.passwordInput {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

button {
  margin-top: 1rem;
  border: none;
  border-radius: 10px;
  padding: 0.5rem 1rem;
}

button:hover {
  opacity: 0.7;
  cursor: pointer;
}


</style>
