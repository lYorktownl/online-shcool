<template>
  <div>
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
      <div class="menu">
        <button @click="toggleMenu" class="menu-btn">
          <svg
            width="17"
            height="14"
            viewBox="0 0 17 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="17" height="2" rx="1" fill="#F15525" />
            <rect y="6" width="17" height="2" rx="1" fill="#F15525" />
            <rect y="12" width="17" height="2" rx="1" fill="#F15525" />
          </svg>
        </button>
      </div>
    </header>

    <div
      v-if="isMenuOpen"
      class="mobile-menu-overlay"
      @click="toggleMenu"
    ></div>

    <div v-if="isMenuOpen" class="mobile-menu">
      <button @click="toggleMenu" class="close-btn">
        <svg
          width="15"
          height="15"
          viewBox="0 0 15 15"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <rect
            y="13.6328"
            width="19.2797"
            height="1.37712"
            transform="rotate(-45 0 13.6328)"
            fill="#BCBCBC"
          />
          <rect
            x="13.6328"
            y="14.6066"
            width="19.2797"
            height="1.37712"
            transform="rotate(-135 13.6328 14.6066)"
            fill="#BCBCBC"
          />
        </svg>
      </button>
      <ul>
        <li><a href="#learn" @click="toggleMenu">Чему вы научитесь</a></li>
        <li><a href="#process" @click="toggleMenu">Процесс обучения</a></li>
        <li><a href="#cost" @click="toggleMenu">Стоимость</a></li>
        <li><a href="#contacts" @click="toggleMenu">Контакты</a></li>
        <li><a href="#register" @click="toggleMenu">Регистрация</a></li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const isMenuOpen = ref(false);

    const toggleMenu = () => {
      isMenuOpen.value = !isMenuOpen.value;
    };

    return {
      isMenuOpen,
      toggleMenu,
    };
  },
});
</script>

<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  background-color: #fff;
  height: 51px;
  max-width: 1160px;
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
.menu {
  display: none;
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
@media (max-width: 740px) {
  .nav {
    display: none;
  }
}
/* Mobile styles */
@media (max-width: 320px) {
  .header {
    width: 300px;
  }
  .logo {
    margin-right: 0;
  }
  .nav {
    display: none;
  }
  .contact {
    margin-right: 10px;
    margin-left: 10px;
  }
  .menu {
    margin-left: auto;
    margin-right: 14px;
    display: block;
  }
  .menu-btn {
    padding: 0;
    border: none;
    background: none;
    cursor: pointer;
  }
  a {
    font-size: 14px;
    line-height: 23px;
    text-align: center;
  }
}

/* Mobile menu styles */
.mobile-menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  z-index: 999;
}

.mobile-menu {
  position: fixed;
  top: 0;
  right: 0;
  width: 100%;
  height: 610px;
  background-color: #fff;
  z-index: 1000;
  display: flex;
  flex-direction: column;
  padding-top: 20px;
}

.mobile-menu .close-btn {
  position: absolute;
  top: 20px;
  right: 20px;
  background: none;
  border: none;
  font-size: 24px;
  cursor: pointer;
}

.mobile-menu ul {
  list-style: none;
  padding: 0;
  font-size: 20px;
  line-height: 20px;
  font-weight: bold;
  margin-top: 80px;
  margin-left: 43px;
}

.mobile-menu ul li {
  margin-bottom: 20px;
}

.mobile-menu ul li a {
  text-decoration: none;
  color: #22253b;
  font-size: 20px;
}
</style>
