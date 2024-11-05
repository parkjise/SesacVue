<template>
  <div>
    <h2 v-if="showName">My name is {{ user.name }}</h2>
    <h2 v-else>이름을 보여줄 수 없습니다</h2>
    <h2 v-if="user.age > 20">당신은 성인입니다</h2>
    <h2 v-else-if="user.age >14 && user.age < 20">당신은 청소년입니다</h2>
    <h2 v-else>당신은 어린이 입니다.</h2>
    <h2 v-if="!showName"> {{ user.name }}</h2>
    <h2 v-show="!showName">{{ user.name }}</h2>
    <ul>
      <template v-if="question === 'frontend'">
        <li>HTML은 재미있나요?</li>
        <li>CSS은 재미있나요?</li>
        <li>JavaScript은 재미있나요?</li>
      </template>
      <div v-else>
        <li>JAVA은 재미있나요?</li>
        <li>Python은 재미있나요?</li>
        <li>C#은 재미있나요?</li>
      </div>
    </ul>
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      question:'frontend',
      showName:true,
      user: {
        name:'Jise Park',
        age:44,
        job:'Web Designer'
      }
    };
  },
  methods: {
    
  },
};
</script>

<style>

</style>
