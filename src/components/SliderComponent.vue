<template>
  <swiper class="swiper" :modules="modules" :slides-per-view="1" navigation>
    <swiper-slide class="slide-container">
      <div class="slide">
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
              Закажите звонок, и наш специалист свяжется с <br />вами в
              ближайшее время
            </p>
            <button class="call-btn" @click="$emit('showModal')">
              Заказать звонок
              <svg
                style="margin-left: 12px"
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z"
                  fill="white"
                />
              </svg>
            </button>
          </div>
          <img
            class="coding-hands"
            src="../assets/icons/codingHands.svg"
            alt="coding hands"
          />
        </div>

        <div class="background">
          <div class="circle-container">
            <div class="circle circle5"></div>
            <div class="circle circle4"></div>
            <div class="circle circle3"></div>
            <div class="circle circle2"></div>
            <div class="circle circle1"></div>
          </div>
        </div>
      </div>
    </swiper-slide>

    <swiper-slide class="slide-container">
      <div class="slide">
        <div class="content">
          <div class="text-block">
            <p class="text-school">
              Обучение<br />
              через практику
            </p>
            <hr />
            <p class="text-calls">
              Всё, что вы узнали, вы тут же начинаете<br />
              применять на практике. Вы сразу видите<br />
              результаты своего труда.
            </p>
            <button class="call-btn" @click="$emit('showModal')">
              Заказать звонок
              <svg
                style="margin-left: 12px"
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z"
                  fill="white"
                />
              </svg>
            </button>
          </div>
          <img
            class="coding-hands"
            src="../assets/icons/manDev.svg"
            alt="coding hands"
          />
        </div>
        <div class="background">
          <div class="circle-container">
            <div class="circle circle5"></div>
            <div class="circle circle4"></div>
            <div class="circle circle3"></div>
            <div class="circle circle2"></div>
            <div class="circle circle1"></div>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide class="slide-container">
      <div class="slide">
        <div class="content">
          <div class="text-block">
            <p class="text-school">
              Весь материал разбит на<br />
              небольшие уроки
            </p>
            <hr />
            <p class="text-calls">
              Теория и практика подаются маленькими <br />порциями. Так вам
              будет легче усваивать новые<br />
              знания.
            </p>
            <button class="call-btn" @click="$emit('showModal')">
              Заказать звонок
              <svg
                style="margin-left: 12px"
                width="16"
                height="16"
                viewBox="0 0 16 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z"
                  fill="white"
                />
              </svg>
            </button>
          </div>
          <img
            class="coding-hands"
            src="../assets/icons/devCoupe.svg"
            alt="coding hands"
          />
        </div>
        <div class="background">
          <div class="circle-container">
            <div class="circle circle5"></div>
            <div class="circle circle4"></div>
            <div class="circle circle3"></div>
            <div class="circle circle2"></div>
            <div class="circle circle1"></div>
          </div>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>



<script lang="ts">

                                    //Привет, я пользовался свайпером впервые и так вышло что к большому сожалению он не дружит с тайпскриптом...
                                    //К еще большему сожалению я выяснил это в самом конце и не смог починить эту ошибку, и поэтому у меня не получилось застилизовать стрелки.
                                    //Если вдруг это все таки возможно сделать, буду премного благодарен, если поясните в фидбеке к коду как это исправить. 
                                    //Это был безусловно классный опыт, сделал для себя полезные выводы, в дальнейшем учту данный нюанс при работе с этой библиотекой.
                                    //Спасибо за понимание.




import { Navigation } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
// Import Swiper styles
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation],
    };
  },
};
</script>

<style scoped>
.swiper {
  margin-top: 23px;
  max-width: 1160px;
  height: 481px;
  font-size: 46px;
  font-weight: 500;
  line-height: 46px;
  text-align: left;
  background-color: #fff;
  border-radius: 48px;
}
/* .swiper-button-prev, .swiper-button-next {

} */
.slide-container {
  overflow: hidden;
  position: relative;
  min-height: 381px;
}
.content {
  display: flex;
  margin-left: 98px;
}
.background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 481px;
  z-index: -8;
}

.circle {
  position: absolute;
  top: 51%;
  right: 240px;
  transform: translate(50%, -50%);
  display: flex;
  align-items: center;
  justify-content: center;

  border: 2px solid white;

  border-image-source: linear-gradient(
    137.25deg,
    #ffffff 21.62%,
    rgba(255, 255, 255, 0) 75.98%
  );

  border-radius: 50%;
  background: linear-gradient(
      0deg,
      rgba(255, 255, 255, 0.3),
      rgba(255, 255, 255, 0.3)
    ),
    linear-gradient(260.38deg, #ffffff -31.68%, rgba(255, 255, 255, 0) 87.52%);
  border: 2px solid;
  box-shadow: 10px 0px 20px 0px #0081aa0f;
  filter: drop-shadow(-80px -11px 18px #0081aa0f);
}
.circle1 {
  border: 2px solid white;
  width: 320px;
  height: 320px;
}
.circle2 {
  border: 2px solid white;
  width: 505px;
  height: 505px;
}

.circle3 {
  border: 2px solid white;
  width: 730px;
  height: 730px;
}

.circle4 {
  border: 2px solid white;
  width: 995px;
  height: 995px;
}
.circle5 {
  border: 2px solid white;
  width: 1374px;
  height: 1374px;
}

.text-school {
  padding-top: 60px;
  max-width: 630px;
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
.call-btn {
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
.call-btn:hover {
  background-color: #38bff2;
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
  margin-right: 77px;
  margin-left: auto;
}
hr {
  margin-left: 0px;
  width: 365.22px;
  color: #dedede;
}

@media (max-width: 320px) {
  .swiper {
    width: 300px;
    height: 609px;
    font-size: 18px;
    line-height: 24px;
    margin-top: 10px;
  }
  .swiper-button-prev,
  .swiper-button-next {
    display: none !important;
  }
  .slide-container {
    height: 609px;
  }

  .content {
    flex-direction: column;
    margin: 0;
    padding: 10px;
    height: 609px;
  }

  .text-school {
    font-size: 24px;
    font-weight: 500;
    line-height: 24px;
    text-align: center;
    padding-top: 30px;
  }

  .text-dev {
    font-size: 24px;
    font-weight: 700;
    text-align: center;
    letter-spacing: 0.3px;
  }

  .text-calls {
    font-size: 12px;
    line-height: 18px;
    text-align: center;
  }

  .call-btn {
    position: static;
    width: 265px;
    height: 70px;
    font-size: 16px;
    margin-top: 15px;
    margin-left: 8px;
  }

  .coding-hands {
    margin: auto auto 45px auto;
    padding: 20px 0;
    width: 210px;
    height: 219px;
  }

  img {
    padding-bottom: 45px;
  }

  hr {
    width: 100%;
  }

  .circle {
    top: 470px;
    right: 50%;
  }
  .circle1 {
    width: 225px;
    height: 225px;
  }
  .circle2 {
    width: 321px;
    height: 353px;
  }

  .circle3 {
    width: 464px;
    height: 512px;
  }

  .circle4 {
    width: 633px;
    height: 696px;
  }
  .circle5 {
    width: 873px;
    height: 961px;
  }
}
</style>
