<template>
	<div>
		<GreetingUser :username="username" :numberOfVisit="numberOfVisit" :siteInfo="siteInfo"/>
		<!-- <GreetingUser username = "dooli" />
		<GreetingUser username = "pororo"/>
		<GreetingUser username = "monkey"/>
		<GreetingUser/> -->
		<button @click="changeName()">Change</button>
	</div>
</template>


<script>
import GreetingUser from "./components/GreetingUser";
export default {
	name: "App",
	components: {
		GreetingUser,
	},
	data(){
		return {
			username:"Hong gil dong",
			numberOfVisit:80,
			siteInfo:{
				name:"Vue Practice",
				teacher:undefined,
				subject:"FrondEnd"
			},
			toggle:false,
		}
	},
	methods: {
		changeName(){
			this.toggle = !this.toggle 
			this.username = this.toggle ? "username" : 'jjTtest!!!!'
		},
	},
};
</script>

<style></style>