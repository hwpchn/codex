<template>
  <div class="login-page">
    <el-row justify="center" align="middle" class="login-row">
      <el-col :span="8">
        <el-card class="box-card">
          <div class="logo">Shipping Logistics</div>
          <el-form :model="form" @submit.prevent="onSubmit" label-position="top">
            <el-form-item label="Email">
              <el-input v-model="form.email" type="email" placeholder="Email" autocomplete="email" />
            </el-form-item>
            <el-form-item label="Password">
              <el-input v-model="form.password" type="password" placeholder="Password" autocomplete="current-password" />
            </el-form-item>
            <el-form-item>
              <el-button type="primary" style="width: 100%" @click="onSubmit">Login</el-button>
            </el-form-item>
          </el-form>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script setup>
import { reactive } from 'vue';
import { ElMessage } from 'element-plus';

const form = reactive({
  email: '',
  password: ''
});

function onSubmit() {
  console.log('Login with:', form);
  // TODO: Replace with real authentication logic
  ElMessage.success('Login attempt');
}
</script>

<style>
.login-page {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(to right, #66a6ff, #89f7fe);
}
.logo {
  text-align: center;
  font-size: 24px;
  color: #409EFF;
  margin-bottom: 20px;
  font-weight: bold;
}
.box-card {
  padding: 20px;
}
.login-row {
  width: 100%;
}
</style>
