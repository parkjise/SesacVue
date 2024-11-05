<template>
   <div>
    <h1 id="title">Hello World{{ userName }}</h1>
    <h1 v-text="userName" v-bind:id="dynamicId"></h1>
    <p>{{ year }}</p>
    <p>{{ user.name }}{{ user.job }}{{ user.age }}</p>
    <p v-html="button"></p>
    <a v-bind:href="url">naver</a>
    <img v-bind:src="image.src" v-bind:alt="image.alt">
    <input v-bind:type="inputType">
    <p v-bind:style="pStyle">V-bind Test</p>
    <p v-bind:style="{color:'red',fontSize: '50px'}">V-bind Test</p>
    <p v-bind:style="{color:'red',fontSize:`${basicSize}px`}">V-bind Test</p>
    <h1 v-bind:style="titleStyle">Hello World{{ userName }}</h1>
    <h1 v-bind:style="[titleStyle,basicStyle]">Hello World{{ userName }}</h1>
    <h2 :class="textDecoration" class="text-orange">Line-through</h2>
    <h2 :class="isDone === true ? 'line-through' : 'highlight'">Line-through</h2>
    <h2 :class="{highlight : isDone === true}">Object형태의 동적 클래스</h2>
    <h2 :class="{
      highlight : isDone === true,
      'text-orange' : userName === 'parkjise'}">Object형태의 동적 클래스</h2>
      <h2 :class="[isDone===true ? 'line-through' : 'highlight',userName === 'parkjise' ? 'text-green' : 'highlight']">Array 형태의 동적 클래스 부여</h2>
      <h2 :class="isDoneT()">TESTESTSTET</h2>
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
      dynamicId:"content",
      url:"https:naver.com",
      image:{
        src:'https://palceimg.com/100/100/any',
        alt:'random image'
      },
      inputType:"text",
      pStyle:"font-size:46px;color:red",
      basicSize:100,
      basicStyle:{
        background:'red'
      },
      titleStyle:{
        'font-weight':'bold',
        fontSize:'120px',
        color:'blue',
        border:"1px solid red"
      },
      textDecoration:'line-through',
      isDone:false
    };
  },
  methods: {
    isDoneT(){
      if(this.isDone === false){
        return this.textDecoration
      }
    }
  },
};
</script>

<style>

</style>
