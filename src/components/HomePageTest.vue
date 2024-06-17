<template>
    <div class="login-page-container">
      <LoginPage/>
      <img src="../assets/2243_U1RVRElPIFBDIDE4MjctMDY.jpg" alt="">
    </div>
  </template>
  
  <script setup>
  import LoginPage from './LoginPage.vue';
  // import RegesterPage from './RegesterPage.vue';
  </script>
  
  <style scoped>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .login-page-container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh; 
    background-image: url('../assets/pexels-jplenio-1103970.jpg'); /* Đường dẫn tới hình ảnh */
    background-size: cover; /* Đảm bảo hình ảnh bao phủ toàn bộ không gian */
    background-position: center; /* Căn giữa hình ảnh */
    background-repeat: no-repeat; /* Không lặp lại hình ảnh */
  }
  
  img {
    margin-left: 50px;
    width: 400px;
    height: auto;
    border-radius: 10px;
  }
  
  h2 {
    text-align: center;
    margin-bottom: 20px;
  }
  </style>
  