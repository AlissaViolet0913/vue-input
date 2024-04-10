<script setup>
import { ref } from 'vue';

const count = ref(0);
const incrementCount = ()=>{
    count.value++;
};
</script>


<template>
    <div>
        <p>カウント： {{ count }}</p>
        <button @click="incrementCount">カウントアップ</button>
    </div>
</template>
