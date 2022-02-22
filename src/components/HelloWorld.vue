<template>
  <div class="container">
    <div class="bg">
      <div class="item item1" @click="goUrl(0)"></div>
      <div class="item item2" @click="goUrl(1)"></div>
      <div class="item item3" @click="goUrl(2)"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {};
  },
  props: {
    msg: String,
  },
  methods: {
    goUrl(n) {
      if (n == 0) {
        window.open("http://10.0.66.108:9090/");
      }
      if (n == 1) {
        window.open("http://10.0.66.108:8090/");
      }
      if (n == 2) {
        window.open("http://10.0.66.108:9099/");
      }
    },
  },
};
</script>

<style scoped>
.bg {
  width: 100%;
  height: 1057px;
  background-image: url("../assets/bg.png");
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.item {
  width: 370px;
  height: 280px;
  margin: 0 10px;
  cursor: pointer;
}
.item:hover {
  transform: scale(1.1, 1.1);
}
.item1 {
  background-image: url("../assets/item1.png");
}
.item2 {
  background-image: url("../assets/item2.png");
}
.item3 {
  background-image: url("../assets/item3.png");
}
</style>
