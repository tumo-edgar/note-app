<template>
    <div class="input-box">
        <input v-model="search" placeholder="Search note..." type="search" />
        <button @click="$emit('onSearch', search)">Search</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const search = ref('')
</script>

<style scoped>
    .input-box {
        display: flex;
        height: 40px;
        max-width: 400px;
        width: 100%;
        gap: 6px;
    }
    .input-box input {
        width: 100%;
        border: 1px solid #fff;
        border-radius: 4px;
        padding-left: 30px;
    }

    .input-box button {
        background: #4CCB90;
        color: white;
        border: 1px solid #fff;
        border-radius: 4px;
    }
</style>