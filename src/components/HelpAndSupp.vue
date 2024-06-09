<template>
  <div class="main">
    <div class="section help-support">
      <img src="../assets/photos/twoMen.png" alt="" />
      <div class="text-block">
        <h2 class="title">Помощь и поддержка</h2>
        <p>
          Если в процессе обучения возникнут сложности,<br />
          вы всегда сможете задать вопрос своему наставнику.
        </p>
        <p>
          Раз в несколько уроков вы будете получать большое задание, <br />
          которое нужно будет сдавать на проверку код-ревьюеру. Он
          внимательно<br />
          изучит ваш код, найдет ошибки и поможет вам стать лучше.
        </p>
      </div>
    </div>
    <div class="section teaching">
      <div class="text-block">
        <h2 class="title">Методика обучения</h2>
        <p>
          Весь учебный материал структурирован по принципу<br />
          «спирального обучения». Сначала вы получаете базовые знания,<br />
          а затем на каждом витке спирали углубляетесь в изученные темы,<br />
          доводя их понимание до совершенства. Такой подход упрощает<br />
          обучение и гарантирует, что вы не пропустите ничего важного.
        </p>
      </div>
      <img src="../assets/photos/coupe.png" alt="" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {};
  },
});
</script>

<style scoped lang="scss">
.main {
  text-align: left;
  display: flex;
  color: #22253b;
  width: 1160px;
  flex-direction: column;
  margin: 0 auto 0 auto;
}
.help-support {
  justify-content: flex-start;
}
.teaching {
  justify-content: flex-end;
}
.section {
  display: flex;
  flex-direction: row;
  gap: 32px;
  border-radius: 10px;
  padding-bottom: 32px;
}
.text-block {
  width: 730px;
  height: 313px;
  background-color: #eaf2f5;
  border-radius: 40px;
  padding-left: 101px;
  margin: 0;
}
.title {
  font-size: 32px;
  font-weight: 400;
  line-height: 30px;
  text-align: left;
  margin: 54px 0 18px 0;
}
p {
  font-size: 16px;
  font-weight: 400;
  line-height: 25px;
  text-align: left;
  margin: 0 0 15px 0;
}
</style>
