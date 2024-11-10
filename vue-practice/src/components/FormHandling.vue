<template>
	<div>
		{{ user }}
		<h1>{{ user.name }}</h1>
		<form>
			<div>
				<label for="name">이름</label>
				<input type="text" id="name" v-model="user.name" @input="setValue" />
			</div>
			<div>
				<label for="age">나이</label>
				<input type="text" id="age" v-model="user.age" />
			</div>
			<div>
				<label for="city">사는곳</label>
				<select type="text" id="city" v-model="user.city">
					<option value="esoul">서울</option>
					<option value="daejeon">대전</option>
					<option value="daegu">대구</option>
					<option value="busan">부산</option>
					<option value="gwangju">광주</option>
				</select>
			</div>
			<div>
				<label for="favorite-food">좋아하는 음식</label>
				<select id="favorite-food" multiple v-model="user.food">
					<option
						v-for="food in foodOption"
						:value="food.code"
						:key="food.code"
					>
						{{ food.label }}
					</option>
				</select>
			</div>
			<div>
				<label for="job">직업</label>
				프로그래머<input
					type="checkbox"
					value="programmer"
					v-model="user.job"
				/>
				가수<input type="checkbox" value="singer" v-model="user.job" />
				교사<input type="checkbox" value="teacher" v-model="user.job" />
			</div>
			<div>
				<label for="job">성별</label>
				남<input type="radio" value="male" v-model="user.gender" /> 여<input
					type="radio"
					value="female"
					v-model="user.gender"
				/>
			</div>
		</form>
	</div>
</template>

<script>
export default {
	name: "App",
	data() {
		return {
			foodOption: [
				{ label: "짜장명", code: "JJ" },
				{ label: "짬뽕", code: "JB" },
				{ label: "탕수육", code: "TS" },
			],
			user: {
				name: "Park Jise",
				age: 0,
				city: "Seoul",
				food: [],
				job: [],
				gentder: [],
			},
		};
	},
	methods: {
		setValue(e) {
			console.log(e.target.value);
			this.user.name = e.target.value;
		},
	},
};
</script>

<style>
label {
	font-size: 22px;
	font-weight: bold;
	margin-right: 1rem;
}
div {
	margin-bottom: 20px;
}
</style>
