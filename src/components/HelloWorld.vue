<template>
  <div class="container">
    <div class="bg">
      <div class="item" @click="goUrl(0)"></div>
      <div class="item" @click="goUrl(1)"></div>
      <div class="item" @click="goUrl(2)"></div>
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
    goUrl(n){
      if(n == 0){
        window.open('http://10.0.66.108:9090/')
      }
      if(n == 1){
        window.open('http://10.0.66.108:8090/')
      }
      if(n == 2){
        window.open('http://10.0.66.108:9099/')
      }
    }
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
  /* border: 1px solid red; */
  width: 382px;
  height: 300px;
  margin: 0 10px;
  cursor: pointer;
}
</style>
