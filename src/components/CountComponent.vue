<script setup>
import { onBeforeMount, onBeforeUpdate, onMounted, onUpdated, ref } from 'vue';

console.log("beforeCreate フック：コンポーネントが初期化される直前");
console.log("created フック：コンポーネントが初期化された直後");

onBeforeMount(()=>{
    console.log("beforeMount フック：DOMにマウントされる直前");
})
onMounted(()=>{
    console.log("mounted フック：DOMにマウントされた直後");
})
onBeforeUpdate(()=>{
    console.log("onBeforeUpdate フック：コンポーネントが再描画される直前");
})
onUpdated(()=>{
    console.log("updated フック：コンポーネントが再描画された直後");
})



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
