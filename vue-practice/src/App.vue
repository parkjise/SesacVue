<template>
  <div>
    <h1>Hello World{{ userName }}</h1>
    <h1 v-text="userName"></h1>
    <p>{{ year }}</p>
    <p>{{ user.name }}{{ user.job }}{{ user.age }}</p>
    <p v-html="button"></p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      userName: "parkjise",
      year: 2024,
      user: {
        name: "jise Park",
        job: "Designer",
        age: 44,
      },
      button: "<button>버튼</button>",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
