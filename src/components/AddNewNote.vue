<template>
    <div class="add-popup">
        <div class="note-form">
             <div class="close">
                <CloseButton @click="$emit('onClose')" />
            </div>
            <h1 class="title">Title</h1>
            <input v-model="title" />
            <textarea v-model="content"></textarea>
            <button class="save" @click="$emit('onSave', title, content)">Save</button>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import CloseButton from './CloseButton.vue';

    const title = ref('')
    const content = ref('')
</script>

<style scoped>
.add-popup{
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: rgba(0,0,0,0.4);
    display: flex;
    justify-content: center;
    align-items: center;
}
.note-form {
    width: 580px;
    padding: 30px 32px 40px;
    background: linear-gradient(114.43deg, rgba(255, 255, 255, 0.6) 4%, rgba(255, 255, 255, 0.1) 100%);
    border: 1px solid #fff;
    display: flex;
    flex-direction: column;
    gap: 18px;
    border-radius: 10px;
    position: relative;
}
.title {
    font-weight: 500;
    font-style: Medium;
    font-size: 18px;
    line-height: 100%;
    letter-spacing: 0%;
    padding: 0;
    text-align: left;
}
.note-form input {
    width: 100%;
    height: 40px;
    border-radius: 4px;
}
.note-form textarea {
    width: 100%;
    resize: none;
    height: 80px;
    border-radius: 4px;
}
.note-form .save {
    width: 100%;
    height: 40px;
    border-radius: 4px;
    background: linear-gradient(90deg, #B4FBF3 0%, #23926F 100%);
    color: #fff;
    font-size: 20px;
    font-weight: 500;
    border: none;
    cursor: pointer;
}
.note-form .save:hover {
    background: linear-gradient(90deg, #56b0a5 0%, #1d7257 100%);
}
.close {
    position: absolute;
    top: 8px;
    right: 8px;
}
</style>