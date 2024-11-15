<template>
  <div>
    <p>Hello {{username}}!!</p>
    <p>오늘이 {{numberOfVisit}}번째 방문입니다</p>
    <p>강사 이름은 {{siteInfo.name}}입니다!!</p>
    <p>강사 이름은 {{siteInfo.teacher}}입니다!!</p>
    <p>강사 이름은 {{siteInfo.subject}}입니다!!</p>

  </div>
  <!-- <div>
    <p>사이트 이름은 {{siteInfo.name}}입니다!!</p>
  </div> -->
</template>

<script>
  export default {
    name:"GreetingUser!!",
    props:{
      // username:String
      username:{
        type:String,
        default:"User!!!!!!!!"
      },
      numberOfVisit:{
        Number
      },
      siteInfo:{
        type:Object,
        default:() => {
          return {name : "-",teacher:"-"}
        }
      }
    }
  }
</script>

<style scoped>

</style>
