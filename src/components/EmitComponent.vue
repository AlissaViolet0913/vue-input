<!-- 子から親にデータを渡す方法(.$emit) -->
<!-- ※親から子にデータを渡すのはpropsを使用 -->

<script>
export default {
    methods:{
        sendMessage(){
            // message:親コンポーネントで受け取るときに使用するイベント名（@イベント名）
            // "子コンポーネントから～"：一緒に渡すデータ
            this.$emit("message", "子コンポーネントから送られたデータ");
        }
    }
}

</script>

<template>
    <button @click="sendMessage">メッセージを送る</button>
</template>
