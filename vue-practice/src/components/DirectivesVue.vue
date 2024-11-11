<template>
  <div>
    <h1>Directives</h1>
    <h2>유저의 이름은 {{ username }}</h2>
    <button @click="changeName">Change name</button>
  </div>
  <div>
    <input type="text" v-focus>
  </div>
  <div>
    <input type="text" v-highlight>
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      username : 'Park Jise'
    };
  },
  directives:{
    focus:{
      mounted(el) {
        el.focus()
      },
    },
    highlight:{
      mounted(el){
        console.log({el})
        el.oninput = () => {
          el.style.background = "sallmon";
          el.style.color = "#fff";
        }
      }
    }
  },  
  methods: {
    changeName(){
      this.username = "Hong gil dong"
    }
  },
};
</script>

<style>

</style>
