<template>
  <h1>Forms</h1>
  <div class="container">
    <LoginForm></LoginForm>


  </div>

</template>

<script setup lang="ts">



import LoginForm from "./components/LoginForm.vue";
</script>

<style scoped>
.container{
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
p{
  text-align: right;
}


</style>
