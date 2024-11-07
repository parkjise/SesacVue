<template>
  <div>
    <!-- <ul>
      <li 
      v-for="(citi,index) in cities.filter((c) => c.province ==='경상도')" :key="index">
        {{ citi.name }}:{{ citi.province }}
      </li>
    </ul> -->
    <ul>
      <template v-for="(citi,index) in cities" :key="index">
        <li v-if="citi.province === '경상도'">
          {{citi.name }}=>{{citi.province }}
        </li>
      </template>
    </ul>
  </div>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      cities:[
        {name:'서울',province:'경기도'},
        {name:'대전',province:'충청도'},
        {name:'대구',province:'경상도'},
        {name:'부산',province:'경상도'},
        {name:'인천',province:'경기도'},
        {name:'광주',province:'전라도'},
      ]
    };
  },
  methods: {
    
  },
};
</script>

<style>

</style>
