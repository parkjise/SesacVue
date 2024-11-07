<template>
  <div>
    {{ fruits }}
  </div>
  <ul>
    <li  v-for="(fruit,idx) in fruits" :key="fruit">
      {{idx + 1}}.{{ fruit }}
    </li>
  </ul>
  <h2 v-for="(value,key,idx) in user" :key="key">
    {{idx + 1}}:::{{ key }} ::: {{ value }}
  </h2>
  <p v-for="n in 10" :key="n">{{ n }}</p>
  <div v-for="(animal,animalIndex) in animals" :key="animalIndex">
    <h2>{{  animal.name}}</h2>
    <h4>Food</h4>
    <ul>
      <li v-for="(food,foodIndex) in animal.favorites" :key="foodIndex">
        {{ food }}
      </li>
    </ul>
    <h4>Size =====>{{ animal.size }} </h4>
    
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      fruits:["banana",'strawberry','apple','melon'],
      user:{
        name:'Park JiSe',
        age:44,
        job:'Web Designer'
      },
      animals:[
        {name:'monkey',size:'medium',favorites:['banana','apple']},
        {name:'lion',size:'big',favorites:['deer','cow']},
        {name:'rat',size:'small',favorites:['cheese','rie']}
      ]
    };
  },
  methods: {
    
  },
};
</script>

<style>

</style>
