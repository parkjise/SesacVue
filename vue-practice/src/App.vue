<template>
	<div>
		<GreetingUser
			:username="username"
			:numberOfVisit="numberOfVisit"
			:siteInfo="siteInfo"
			id="greeting"
		/>
		<!-- <GreetingUser username = "dooli" />
		<GreetingUser username = "pororo"/>
		<GreetingUser username = "monkey"/>
		<GreetingUser/> -->
		<button @click="changeName()">Change</button>
	</div>
	<ul>
		<li v-for="product in products" :key="product.id">
			{{ product }}
		</li>
		<ProductList :products="products" />
	</ul>
</template>

<script>
import GreetingUser from "./components/GreetingUser";
import ProductList from "./components/ProductList";
export default {
	name: "App",
	components: {
		GreetingUser,
		ProductList,
	},
	data() {
		return {
			username: "Hong gil dong",
			numberOfVisit: 80,
			siteInfo: {
				name: "Vue Practice",
				teacher: undefined,
				subject: "FrondEnd",
			},
			toggle: false,
			products: [
				{
					id: 0,
					name: "TV",
					price: 500000,
					company: "LG",
				},
				{ id: 1, name: "전자렌지", price: 500000, company: "삼성" },
				{ id: 2, name: "오븐", price: 500000, company: "한화" },
				{ id: 3, name: "냉장고", price: 500000, company: "대우" },
				{ id: 4, name: "에어컨", price: 500000, company: "휘센" },
			],
		};
	},
	methods: {
		changeName() {
			this.toggle = !this.toggle;
			this.username = this.toggle ? "username" : "jjTtest!!!!";
		},
	},
};
</script>

<style></style>
