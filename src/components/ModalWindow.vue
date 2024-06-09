<template>
    <div class="modal" v-if="isVisible">
      <div class="modal-content">
        <span class="close" @click="closeModal">&times;</span>
        <h2>Заказать звонок</h2>
        <form @submit.prevent="handleSubmit">
          <label for="name">Имя</label>
          <input type="text" id="name" v-model="formData.name" placeholder="ваше имя" required />
  
          <label for="phone">Телефон</label>
          <input type="tel" id="phone" v-model="formData.phone" placeholder="+7 XXX - XXX - XX -XX" required />
  
          <label for="email">Email</label>
          <input type="email" id="email" v-model="formData.email" placeholder="mail@site.com" required />
  
          <label for="message">Сообщение</label>
          <textarea id="message" v-model="formData.message" placeholder="Ваше сообщение ..." required></textarea>
  
          <p>
            Нажимая кнопку "Отправить", соглашаетесь с <br>
            <a href="#" class="privacy-policy">политикой конфиденциальности</a>
          </p>
  
          <button type="submit" class="submit-btn">Отправить <svg style="margin-left:12px;" width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M1.00188 13.5151C0.611353 13.9056 0.611353 14.5388 1.00188 14.9293C1.3924 15.3198 2.02557 15.3198 2.41609 14.9293L1.00188 13.5151ZM15.709 1.2222C15.709 0.669913 15.2613 0.222198 14.709 0.222198L5.70898 0.222198C5.1567 0.222198 4.70898 0.669914 4.70898 1.2222C4.70899 1.77448 5.1567 2.2222 5.70898 2.2222L13.709 2.2222L13.709 10.2222C13.709 10.7745 14.1567 11.2222 14.709 11.2222C15.2613 11.2222 15.709 10.7745 15.709 10.2222L15.709 1.2222ZM2.41609 14.9293L15.4161 1.9293L14.0019 0.515091L1.00188 13.5151L2.41609 14.9293Z" fill="white"/>
              </svg></button>
        </form>
      </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
    props: {
      isVisible: {
        type: Boolean,
        required: true,
      },
    },
    emits: ['close', 'submit'],
    setup(props, { emit }) {
      const formData = ref({
        name: '',
        phone: '',
        email: '',
        message: '',
      });
  
      const closeModal = () => {
        emit('close');
      };
  
      const handleSubmit = () => {
        emit('submit', formData.value);
        closeModal();
      };
  
      return {
        formData,
        closeModal,
        handleSubmit,
      };
    },
})
</script>

<style lang="scss" scoped>
.modal {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgb(0,0,0);
    background-color: rgba(0,0,0,0.4);
  }
  
  .modal-content {
    background-color: #fefefe;
    margin: auto;
    padding: 20px;
    border: 1px solid #888;
    width: 635px;
    height: 100vh;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    position: relative;
  }
  
  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
    position: absolute;
    right: 15px;
    top: 10px;
    cursor: pointer;
  }
  
  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }
  
  h2 {
    text-align: center;
    margin-bottom: 46px;
    margin-top: 80px;
  }
  
  label {
    display: block;
    margin-bottom: 16px;
    margin-top: 24px;
font-size: 16px;
font-weight: 500;
line-height: 18.83px;
font-weight: bold;

  }
  
  input, textarea {
    width: calc(100% - 20px);
    height: 75px;
    padding: 30px;
    border: 1px solid #9F9F9F;
    border-radius: 10px;
    box-sizing: border-box;
font-size: 16px;
font-weight: 400;
line-height: 18.56px;


  }
  
  textarea {
    height: 120px;
  }
  
  p {
    font-size: 12px;
    color: #9F9F9F;
    margin-bottom: 25px;
  }
  
  .privacy-policy {
    color: #f15525;
    text-decoration: none;
  }
  
  .privacy-policy:hover {
    text-decoration: underline;
  }
  
  .submit-btn {
    display: block;
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
  }
  
  .submit-btn:hover {
    background-color: #f15525;
  }
</style>
  
