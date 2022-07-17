<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app">
    <HelloWorld />
    <Shoppingcart />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Shoppingcart from "./components/Shoppingcart.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    Shoppingcart,
  },
};
</script>

<style>
body {
  background: #f0f8ff;
}
#app {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #2c3e50;
  margin-top: 60px;
}
.app {
  width: 750px;
}
@media (max-width: 420px) {
  .app {
    max-width: 420px;
  }
}
@media (max-width: 820px) {
  .app {
    max-width: 750px;
  }
}
</style>
