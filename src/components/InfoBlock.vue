<template>
  <div class="code-block">
    <h1 class="title">
      Обучение в CoDe — это <br />
      удобно и результативно
    </h1>
    <div class="features">
      <div class="feature" v-for="(feature, index) in features" :key="index">
        <img :src="require(`@/assets/icons/${feature.icon}`)" alt="Icon" />
        <h2>{{ feature.title }}</h2>
        <p>{{ feature.description }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

interface Feature {
  icon: string;
  title: string;
  description: string;
}

export default defineComponent({
  setup() {
    const features = ref<Feature[]>([
      {
        icon: "code.png",
        title: "Огромное количество практики",
        description:
          "Более 500 самостоятельных заданий и 20 полноценных больших проектов",
      },
      {
        icon: "blackhole.png",
        title: "Современные методики обучения",
        description:
          "Спиральное обучение: погружаемся в материал постепенно, виток за витком",
      },
      {
        icon: "monitor.png",
        title: "Простое и понятное изложение",
        description: "Вместо заумных терминов — примеры из реального мира",
      },
      {
        icon: "calendar.png",
        title: "Гибкий график занятий",
        description: "Учитесь в любое время в удобном для вас темпе",
      },
      {
        icon: "chat.png",
        title: "Прямая связь с опытными программистами",
        description: "Задавайте вопросы и отправляйте свой код на проверку",
      },
      {
        icon: "coin.png",
        title: "Оплата небольшими частями",
        description:
          "Платите только за тот материал, который сейчас изучаете, а не за весь курс сразу",
      },
      {
        icon: "payment.png",
        title: "Быстрый и легкий возврат",
        description:
          "Если передумаете учиться — вернем деньги за 3 рабочих дня",
      },
    ]);
    return {
      features,
    };
  },
});
</script>

<style scoped>
.code-block {
  text-align: center;
  margin: 0 auto 60px auto;
  max-width: 1160px;
}
.title {
  font-size: 46px;
  font-weight: 600;
  line-height: 46px;
  text-align: center;
  margin-top: 60px;
  margin-bottom: 32px;
}
.features {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}

.feature {
  justify-content: center;
  background-color: #f0f4f8;
  border-radius: 30px;
  width: 270px;
  height: 254px;
}

.feature img {
  width: 58px;
  height: 58px;
  margin-top: 50px;
}

.feature h2 {
  font-size: 16px;
  margin-bottom: 10px;
  font-family: Gilroy;
  font-weight: 400;
  line-height: 18.5px;
  text-align: center;
  width: 166px;
  margin: auto;
  margin-top: 18px;
}

.feature p {
  font-family: Gilroy;
  font-size: 13px;
  font-weight: 400;
  line-height: 15px;
  text-align: center;
  width: 200px;
  margin: auto;
  padding-top: 10px;
}
</style>
