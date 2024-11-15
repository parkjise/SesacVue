<template>
  <div>
    <h1>Watchers</h1>
    <h2>current money :: {{ money }}</h2>
    <div>
      <button @click="money += 100">earn money</button>
      <button @click="money -= 100">spend moeny</button>
    </div>
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      money:15000
    };
  },
  computed:{
    
  },

  watch:{
    money(newValue,oldValue){
      console.log(newValue,oldValue)
      if(newValue > 16000){
        console.log('dffdkfdjfkdjfkf')
      }
    }
  },

  methods: {
    
  },
};
</script>

<style>

</style>
