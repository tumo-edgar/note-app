<template>
    <div class="card">
        <div class="close">
            <CloseButton />
        </div>
        <p class="title">My Title</p>
        <p class="content">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Odio et, temporibus obcaecati est quas vero iste, dolorum voluptate libero praesentium fugit, debitis delectus itaque optio. Dolorum, aut veniam! Id, obcaecati.
        </p>
        <p class="time">05-07-2025 20:30</p>
    </div>
</template>

<script setup>
import CloseButton from './CloseButton.vue';
</script>

<style scoped>
    .card {
        position: relative;
        width: 300px;
        height: 210px;
        border: 1px solid #fff;
        border-radius: 14px;
        background: linear-gradient(114.43deg, rgba(255, 255, 255, 0.6) 4%, rgba(255, 255, 255, 0.1) 100%);
        padding: 18px 20px 8px 20px;
    }

    .title {
        font-weight: 600;
        font-style: 500;
        font-size: 28px;
        line-height: 100%;
        letter-spacing: 0%;
        margin-bottom: 20px;
    }

    .content {
        font-weight: 400;
        font-size: 18px;
        line-height: 100%;
        letter-spacing: 0%;
        width: 100%;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 4;
        overflow: hidden;
        min-height: 72px;
    }
    .time {
        margin-top: 40px;
        text-align: right;
        color: #797979;
        font-size: 14px;
    }
    .close {
        position: absolute;
        top: 8px;
        right: 8px;
        opacity: 0;
        transition: 0.3s;
    }
    .card:hover .close {
        opacity: 1;
    }
</style>