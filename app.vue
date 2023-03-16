<template>
  <head>
    <title>Online Album</title>
  </head>
  <div
    id="app"
  >
  <!-- modal 2 -->
 <div class="box">
  <div class="modal-container" id="m2-o" style="--m-background: hsla(0, 0%, 0%, .4);">
    <div class="modal">
      <h1 class="modal__title">Mau album kece seperti ini juga?</h1>
      <p class="modal__text">Yuk, dapatkan promo 50% khusus 100 pembeli pertama, hanya sampai 30 April 2023. Klik tombol untuk hubungi kami <span>
        <button class="whatsapp" id="buttonwa" role="link" onclick=" window.open('http://wa.me/6281333387057?text=Halo, saya minat album onlinenya')">
        <i class="fab fa-whatsapp"></i>
        </button>
      </span> </p>
        
        <a href="#m2-c" class="link-2"></a>
  </div>
</div>
</div>
<!-- /modal 2 -->

  <Flipbook class="flipbook" :pages="pages"
      v-slot="flipbook"
      ref="flipbook"
     
  >
    <div class="action-bar">
        <left-icon
          class="btn left"
          :class="{ disabled: !flipbook.canFlipLeft }"
          @click="flipbook.flipLeft"
        />
        <plus-icon
          class="btn plus"
          :class="{ disabled: !flipbook.canZoomIn }"
          @click="flipbook.zoomIn"
        />
        <span class="page-num">
          Halaman {{ flipbook.page }} dari {{ flipbook.numPages }}
        </span>
        <minus-icon
          class="btn minus"
          :class="{ disabled: !flipbook.canZoomOut }"
          @click="flipbook.zoomOut"
        />
        <right-icon
          class="btn right"
          :class="{ disabled: !flipbook.canFlipRight }"
          @click="flipbook.flipRight"
        />
        <a href="#m2-o" class="link-1" id="m2-c">
          <info-variant
          class="btn info"
        />
        </a>
      </div>
  </Flipbook>
  <div class="social">
		<h3 class="title" font-family="Avenir">Follow us on :</h3>
        <button class="youtube" id="buttonyt" role="link" onclick="window.open('http://www.youtube.com')">
            <i class="fab fa-youtube"></i>
        </button>
        <button class="facebook" id="buttonfb"
        role="link"
        onclick="window.open('http://www.facebook.com')">
            <i class="fab fa-facebook-f"></i>
        </button>
        <button class="instagram" id="buttonig"
        role="link"
        onclick="window.open('http://www.instagram.com')">
            <i class="fab fa-instagram"></i>
        </button>
        <button class="tiktok" id="buttontt"
        role="link"
        onclick="window.open('http://www.tiktok.com')">
            <i class="fab fa-tiktok"></i>
        </button>
        <button class="twitter" id="buttontw"
        role="link"
        onclick="window.open('http://www.twitter.com')">
            <i class="fab fa-twitter"></i>
        </button>
        <button class="whatsapp" id="buttonwa"
        role="link"
        onclick="window.open('http://www.whatsapp.com')">
            <i class="fab fa-whatsapp"></i>
        </button>
    </div>
  </div>
</template>

<script setup >


import Flipbook from 'flipbook-vue'
import 'vue-material-design-icons/styles.css'
import LeftIcon from 'vue-material-design-icons/ChevronLeftCircle'
import RightIcon from 'vue-material-design-icons/ChevronRightCircle'
import PlusIcon from 'vue-material-design-icons/MagnifyPlus'
import MinusIcon from 'vue-material-design-icons/MagnifyMinus'
import InfoVariant from 'vue-material-design-icons/InformationVariant'

const pages = [
  null,
  'images-large/1.jpg',
  'images-large/2.jpg',
  'images-large/3.jpg',
  'images-large/4.jpg',
  'images-large/5.jpg',
  'images-large/6.jpg',
// 'https://imagizer.imageshack.com/img922/247/dmEZgH.jpg',
// 'https://imagizer.imageshack.com/img922/8053/CKBYY8.jpg',
// 'https://imagizer.imageshack.com/img922/2277/oYgiL9.jpg',
// 'https://imagizer.imageshack.com/img922/2116/T4lFbT.jpg',
// 'https://imagizer.imageshack.com/img923/2428/zvFsk8.jpg',
// 'https://imagizer.imageshack.com/img923/4234/LkFuJP.jpg',


]


</script>

<style>
 @import './public/css/style.css';
 @import './public/css/modal.css';
 @import './public/css/social.css';
 @import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.1/css/all.min.css");
 @import url("https://fonts.googleapis.com/css?family=Gruppo");

</style>


