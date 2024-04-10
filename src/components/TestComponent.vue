
<!-- 親コンポーネントから子コンポーネントにデータを渡すにはpropsを使用 -->
<!-- 子側：difineProps関数を使用、表示するときには{{名前}}と記載 -->

<script setup>
defineProps({
    text: String
});
const dataTest = "これはテストデータです！";
</script>


<!-- {{}}: マスタッシュ構文 -->
<template>
    <p>{{ text }}</p>
    <p>{{ dataTest }}</p>
    <!-- <p v-text="dataTest"></p> -->

</template>
