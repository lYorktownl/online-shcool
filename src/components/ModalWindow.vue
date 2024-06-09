<template>
    <div v-if="show" class="modal">
        <div class="modal-content">
        <span class="close" @click="close">&times;</span>
        <form @submit.prevent="submitForm">
            <input type="text" placeholder="Ваше имя" v-model="name" required />
            <input type="tel" placeholder="Ваш телефон" v-model="phone" required />
            <button type="submit">Отправить</button>
        </form>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup () {
        

        return {}
    }
})
</script>

<style scoped>

</style>