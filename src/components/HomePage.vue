<template>
  <div class="home-page-container">
    <div class="overlay"></div>
    <div class="content">
      <div class="header">
        <div class="content">
          <div class="logo element">
            <a href="#"><img src="../assets/logo.png" alt="logo" class="img_logo"></a>
          </div>
          <div class="element"><a href="#" class="link_page">Giới thiệu</a></div>
          <div class="element">
            
              <div @click="toggleHotelList" class="link_page btn_list_hotel">Khu vực của bạn</div>
              <div v-if="showHotelList" class="hotel-list">
                <h2 class="title">Danh sách khách sạn</h2>
                <ul style="display: flex; flex-direction: column;">
                  <li v-for="hotel in hotels" :key="hotel.id" >
                    <h3>{{ hotel.name }} </h3>
                    <p>{{ hotel.location }}</p>
                  </li>
                </ul>
              </div>

          </div>
      
          <div class="element"></div>
        </div>
        <div class="content">
          <div class="element"><a href="#" class="link_page">Register <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" style="padding-top: 7px;"><path fill="currentColor" d="M15 4a4 4 0 0 0-4 4a4 4 0 0 0 4 4a4 4 0 0 0 4-4a4 4 0 0 0-4-4m0 1.9a2.1 2.1 0 1 1 0 4.2A2.1 2.1 0 0 1 12.9 8A2.1 2.1 0 0 1 15 5.9M4 7v3H1v2h3v3h2v-3h3v-2H6V7zm11 6c-2.67 0-8 1.33-8 4v3h16v-3c0-2.67-5.33-4-8-4m0 1.9c2.97 0 6.1 1.46 6.1 2.1v1.1H8.9V17c0-.64 3.1-2.1 6.1-2.1"/></svg></a></div>
          <div class="element"><a href="#" class="link_page">Sign in<svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"  style="padding-top: 7px;"><path fill="currentColor" d="M12 21v-2h7V5h-7V3h7q.825 0 1.413.588T21 5v14q0 .825-.587 1.413T19 21zm-2-4l-1.375-1.45l2.55-2.55H3v-2h8.175l-2.55-2.55L10 7l5 5z"/></svg></a>
            
          </div>
        </div>
      </div>
      <div class="body">
        <p>Here is some body content. You can add anything you want here.</p>
        <img src="#" alt="Sample Image">

      
      </div>
      <div class="footer">
        <p>&copy; 2024 Your Company. All rights reserved.</p>
      </div>
    </div>
  </div>
</template>



<script setup>
import { ref } from 'vue';

// Dữ liệu danh sách khách sạn
const hotels = [
  { id: 1, name: "Khách sạn hoàng gia ", location: "Hà Nội", image: "../assets/hotel1.jpg" },
  { id: 2, name: "khách sạn hoàng yen", location: "TP Hồ Chí Minh", image: "../assets/hotel2.jpg" },
  { id: 3, name: "khách sạn hoàng dong", location: "Đà Nẵng", image: "../assets/hotel3.jpg" }
];

// Trạng thái hiển thị danh sách khách sạn
const showHotelList = ref(false);

// Hàm để thay đổi trạng thái hiển thị danh sách khách sạn
const toggleHotelList = () => {
  showHotelList.value = !showHotelList.value;
};
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
.btn_list_hotel{
  position: relative;
}

.link_page{
  display: inline-block;
  color: black;
  font-size: 20px;
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
.title{
  font-size: 24px;
}
.hotel{
  position: absolute ;
  top: 0;
  bottom: 0;
  left: 0;
  margin: 0;
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

.hotel-list {
  background-color: white;
  position: absolute ;
  top: 75px;
  margin: 0;
  color :black;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}

.hotel-list h2 {
  font-size: 20px;
  margin-bottom: 10px;
}
.hotel-list h3 {
  font-size: 16px;
  margin-bottom: 10px;
}
.hotel-list ul {
  list-style: none;
  padding: 0;
}

.hotel-list li {
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 10px;
  padding: 10px;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}
.hotel-list p {
  font-size: 10px;
  font-style: italic;
  margin-left: 50px;
}
</style>

