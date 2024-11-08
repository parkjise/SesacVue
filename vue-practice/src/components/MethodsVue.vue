<template>
  <div>
    <div>5년뒤 :: {{add(5) }}</div>
    <div>동갑의 10명이 있따면 나의 총 합은{{ mutiply(age,10) }}</div>
    <div>{{getTotalScore(20)  }}</div>
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      age:44
    };
  },
  methods: {
    add(num){
      console.log(num)
      return this.age + num
    },
    mutiply(num1,num2){
      return num1 * num2
    },
    getTotalScore(num){
      return this.mutiply(num,num)
    }
  },
};
</script>

<style>

</style>
