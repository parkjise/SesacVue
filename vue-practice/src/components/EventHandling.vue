<template>
	<div>
		<h1>{{ name }}</h1>
		<button @click="changeName">Change Name</button>
		<button @mouseover="name = 'desigin'" @mouseleave="name = 'honggildong'">
			Change Name
		</button>
		<a href="https://naver.com" @click.prevent="movePage">네이버로 이동</a>
		<h2>{{ number }}</h2>
		<button @click="increment(1)">숫자1증가</button>
		<button @click="drcrement(1)">숫자1감소</button>
		<button @click="increment(5)">숫자5증가</button>
		<button @click="drcrement(5)">숫자5감소</button>
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			name: "Park JiSe",
			number: 0,
		};
	},
	methods: {
		changeName() {
			this.name = "Jise Park";
		},
		movePage(e) {
			const check = confirm("페이지를 이동하시겠습니까?");
			if (check === true) {
				console.log("페이지 이동");
			} else {
				e.preventDefault();
				console.log("페이지 이동 안함");
			}
		},
		increment(num) {
			this.number += num;
		},
		drcrement(num) {
			this.number -= num;
		},
	},
};
</script>

<style></style>
