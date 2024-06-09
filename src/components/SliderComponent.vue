<template>
  <swiper
    class="swiper"
    :modules="modules"
    :slides-per-view="1"
    navigation
  >
    <swiper-slide class="slide">
      <div class="background">
        <div class="content">
          <div class="text-block">
            <p class="text-school">
              Школа <span class="skobka">{</span>
              <span class="text-dev">программирования</span>
              <span class="skobka">}</span>для тех, кому нужны реальные навыки,
              <br />а не просто сертификат
            </p>
            <hr />
            <p class="text-calls">
              Закажите звонок, и наш специалист свяжется с <br />вами в ближайшее
              время
            </p>
            <button class="call-btn" @click="$emit('showModal')">Заказать  звонок <svg style="margin-left:12px;" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z" fill="white"/>
            </svg>
            </button>
          </div>
          <img class="coding-hands" src="../assets/icons/codingHands.svg" alt="coding hands">      
        </div>
      </div>
    </swiper-slide>
  
      <swiper-slide class="slide">
        <div class="background">
          <div class="content">
            <div class="text-block">
              <p class="text-school">
                Обучение через практику
              </p>
              <hr />
              <p class="text-calls">
                Всё, что вы узнали, вы тут же начинаете<br> применять на практике. Вы сразу видите<br> результаты своего труда.
              </p>
              <button class="call-btn" @click="$emit('showModal')">Заказать  звонок <svg style="margin-left:12px;" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z" fill="white"/>
              </svg>
              </button>
            </div>
            <img class="coding-hands" src="../assets/icons/manDev.svg" alt="coding hands">      
          </div>
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <div class="background">
          <div class="content">
            <div class="text-block">
              <p class="text-school">
                Весь материал разбит на<br> небольшие уроки
              </p>
              <hr />
              <p class="text-calls">
                Теория и практика подаются маленькими <br>порциями. Так вам будет легче усваивать новые<br> знания.
              </p>
              <button class="call-btn" @click="$emit('showModal')">Заказать  звонок <svg style="margin-left:12px;" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z" fill="white"/>
              </svg>
              </button>
            </div>
            <img class="coding-hands" src="../assets/icons/devCoupe.svg" alt="coding hands">      
          </div>
        </div>
      </swiper-slide>
    </swiper>     
</template>
<script lang="ts"> 
// import Swiper core and required modules
import { Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

// Import Swiper styles
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    
    return {
      modules: [Navigation],
    };
  },
};
</script>

<style scoped>
.swiper {
  margin-top: 23px;
  width: 1160px;
  height: 481px;
  font-size: 46px;
  font-weight: 500;
  line-height: 46px;
  text-align: left;
  background-color: #fff;
  border-radius: 48px;
}
.content {
  display: flex;;
  margin-left: 98px;
}
.text-school {
  padding-top: 60px;
  width: 638px;
  margin: 0;
}
.text-dev {
  font-size: 46px;
  font-weight: 700;
  line-height: 46px;
  text-align: left;
}
.text-calls {
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
}
.call-btn{
  position: fixed;
  background-color: #f15525;
  width: 256px;
  height: 70px;
  border-radius: 82px;
  border: none;
  color: #fff;
  font-size: 20px;
  font-weight: 400;
  line-height: 19.34px;
  letter-spacing: -0.03em;
  text-align: center;
  cursor: pointer;
  bottom: 56px;

}
.call-btn:hover{
    background-color: #38BFF2;
  }
.skobka {
  color: #f15525;
}
.coding-hands {
  padding-left: 40px;
  padding-top: 76px;
}

img {
  width: 306px;
  height: 320px;
}
hr {
  margin-left: 0px;
  width: 365.22px;
  color: #dedede;
}
</style>