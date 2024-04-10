<script setup>
// const number = 15;
const number = 5;
</script>

<template>
    <div>
        <!-- <p v-if="number < 10 ">数字は10より小さいです</p>
        <p v-else>数字は10より大きいです</p> -->

        <p v-show="number < 10">数字は10より小さいです</p>
        <!-- v-elseに相当するものはない -->
    </div>
</template>


<!-- v-ifとv-showの違い：非表示の場合、v-showだと要素自体は存在したままdisplay:noneで非表示になる -->
<!-- 再表示するためにコストがv-ifの方が多い -->
<!-- ⇒条件が頻繁に切り替わる場合はv-showを使用 -->
