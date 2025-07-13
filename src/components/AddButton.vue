<template>
    <button class="add-btn">
       <i class="fa-solid fa-plus"></i>
    </button>
</template>

<script setup>
    
</script>

<style scoped>
.add-btn {
    position: fixed;
    bottom: 100px;
    right: 100px;
    width: 68px;
    height: 68px;
    border: 2px solid #fff;
    border-radius: 50%;
    font-size: 40px;
    background: #4CCB90;
    color: #fff;
    cursor: pointer;
    transition: 0.3s;
}
.add-btn:hover {
    background: #38976b;
    transform: scale(1.2);
}

</style>