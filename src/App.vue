<template>
  <div class="login-container">
    <div class="logo">Shipping Logistics</div>
    <el-form :model="form" @submit.prevent="onSubmit">
      <el-form-item>
        <el-input v-model="form.email" type="email" placeholder="Email" autocomplete="email" />
      </el-form-item>
      <el-form-item>
        <el-input v-model="form.password" type="password" placeholder="Password" autocomplete="current-password" />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" style="width: 100%" @click="onSubmit">Login</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const form = reactive({
  email: '',
  password: ''
});

function onSubmit() {
  console.log('Login with:', form);
  alert('Login attempt');
}
</script>

<style>
body {
  background-color: #f5f5f5;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-family: Arial, sans-serif;
}
.login-container {
  padding: 40px;
  background-color: #ffffff;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  width: 400px;
}
.logo {
  text-align: center;
  margin-bottom: 20px;
  font-size: 24px;
  color: #409EFF;
}
</style>
