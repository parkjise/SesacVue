<template>
  <div>
    {{ address }}
  </div>
  <p>내가 받은 점수의 합은 {{ gradeSum }}</p>
  <p>내가 받은 점수의 합은 {{ getTotalScore() }}</p>
</template>

<script>
  export default {
  name: "App",
  data() {
    return {
      username : 'Park Jise',
      address1:"성남시",
      address2:"분당구",
      address3:"정자로",
      grade:{
        math:70,
        eng:60,
        sci:55,
        kor:90
      }
    };
  },
  computed:{
    address(){
      return `${this.address1}${this.address2}${this.address3}`;
    },
    gradeSum(){
      const{math,eng,sci,kor} = this.grade
      return math+eng+sci+kor
    }
  },
  methods: {
    getTotalScore(){
      const{math,eng,sci,kor} = this.grade
      return math+eng+sci+kor
    }
  },
};
</script>

<style>

</style>
