<template>
    <div class="card">
        <h1>{{ props.name }}</h1>
        <h2>{{ props.age }}</h2>
        <h1>{{ counter }}</h1>

        <button @click="pixShatacnel">Click me</button>
    </div>
</template>

<script setup>
import { ref, defineProps } from 'vue'

const props = defineProps(['name', 'age', 'count'])

let counter = ref(props.count)

function pixShatacnel() {
    counter.value++
}
</script>

<style>
    .card {
        width: 300px;
        height: 300px;
        border: 1px solid gray;
        border-radius: 6px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
</style>