<template>
  <div class="home-page-container">
    <div class="overlay"></div>
    <div class="content">
      <div class="header">
      <div class="content">
        <div class="logo element" >
          <a href=""><img src="../assets/logo.png" alt="logo" class="img_logo" ></a></div>
        <div class="element"><a href="" class="link_page">Giới thiệu</a></div>
        <div class="element"><button>Danh mục khách sạn</button></div>
        <div class="element"></div>
      </div>
      <div class="content">
        <div class="element"><a href="" class="link_page">Login</a></div>
        <div class="element"><a href="" class="link_page">Sign in</a></div>
        </div>
      </div>
      <div>
       
      </div>
      <div class="body">
        <p>Here is some body content. You can add anything you want here.</p>
        <img src="" alt="Sample Image">
      </div>
      <div class="footer">
        <p>&copy; 2024 Your Company. All rights reserved.</p>
      </div>
    </div>
  </div>
</template>


<script setup>
// import LoginPage from './LoginPage.vue';
// import RegesterPage from './RegesterPage.vue';
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.content{
  display: flex;

  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}
.home-page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-image: url('../assets/pexels-jplenio-1103970.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
}
.element{
  text-align: center;

  margin: 10px;
}
.link_page{
  display: inline-block;
  color: black;
  font-size: 24px;
  text-decoration: none;
  transition: background-color 0.3s ease;
  padding: 0 10px;
  border-radius: 10px;
}
.link_page:hover {
  background-color: #8E8E79; /* Brightened background color on hover */
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); /* Lớp phủ màu đen với độ trong suốt 50% */
  z-index: 1;
}

.content {
  position: relative;
  z-index: 2;
  color: white;
  text-align: center;
  padding: 20px;
}

.body, .footer {
  margin: 10px 0;
}
.header {
  background-color: #FDFDF5;
  display: flex;
  position: fixed;
  height: 75px;
  top: 0;
  left: 0;
  right: 0;
}
.header h1 {
  font-size: 36px;
  margin-bottom: 20px;
}

.body p {
  font-size: 18px;
  margin-bottom: 20px;
}

.img_logo {
  width: 60px;
  height: auto;
  border-radius: 10px;
  transition: transform 0.3s ease-in-out;
}

img:hover {
  transform: scale(1.1);
}

.footer p {
  font-size: 14px;
  opacity: 0.8;
}
</style>

