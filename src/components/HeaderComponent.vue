<template>
  <header class="header">
    <div class="logo">
      <p>
        <span class="highlight1">C</span>o<span class="highlight2">D</span>e
      </p>
    </div>
    <nav class="nav">
      <ul>
        <li><a href="#learn">Чему вы научитесь</a></li>
        <li><a href="#process">Процесс обучения</a></li>
        <li><a href="#cost">Стоимость</a></li>
        <li><a href="#contacts">Контакты</a></li>
      </ul>
    </nav>
    <div class="contact">
      <a href="tel:+74993489396">+7 (499) 348 93 96</a>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  background-color: #fff;
  height: 51px;
  width: 1160px;
  border-radius: 75px;
  margin: 24px auto 0 auto;
}

.logo {
  font-size: 24px;
  font-weight: 500;
  margin-right: 49px;
  margin-left: 34px;
}

.logo .highlight1 {
  color: #f15525;
}

.logo .highlight2 {
  color: #0d99ff;
}
.nav ul {
  justify-self: none;
  display: flex;
  list-style: none;
  padding: 0;
  margin-right: 41px;
}

.nav ul li {
  margin-right: 20px;
}

.nav ul li a {
  text-decoration: none;
  color: #333;
}
.contact {
  margin-left: auto;
  margin-right: 33px;
  a {
    text-decoration: none;
    color: #38bff2;
    font-size: 16px;
    font-weight: 400;
    line-height: 23px;
    text-align: left;
  }
}
</style>
