<!-- ルートコンポーネント -->

<!-- JavaScript部分 -->
<script setup>
import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
// import TestComponent from './components/TestComponent.vue'
// import ListComponent from './components/ListComponent.vue';
// import IfComponent from './components/IfComponent.vue';
// import CountComponent from './components/CountComponent.vue'
import EmitComponent from './components/EmitComponent.vue';

// 子コンポーネントから値を受け取る、Composition API
import { ref } from 'vue';
const receivedMessage = ref(''); //リアクティブな変数を作成、初期値を設定する
const handleMessageFromChild = (message) => {
  receivedMessage.value = message; //refでラップされた変数にアクセスする場合には.valueを使う
};
</script>

<!-- HTML部分 -->
<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <!-- <TheWelcome /> -->
    <!-- <TestComponent text="propsを試してみた!"/> -->
    <!-- <ListComponent/> -->
    <!-- <IfComponent/> -->
    <!-- <CountComponent/> -->

    <div>
      <EmitComponent  @message="handleMessageFromChild" />
      <p>{{ receivedMessage }}</p>
    </div>
  </main>
</template>

<!-- CSS部分 -->
<style>
@import './assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
