
<script setup>
const fruitsList = [
    { id: 0, name: "リンゴ" },
    { id: 1, name: "いちご" },
    { id: 2, name: "バナナ" },
];
</script>


<template>
    <ul>
        <li v-for="fruit in fruitsList" :key="fruit.id">{{ fruit.name }}</li>
    </ul>
</template>
