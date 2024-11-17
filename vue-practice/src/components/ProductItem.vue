<template>
	<li>
		<p class="title">제품명</p>
		<p><img src="htttps://placeimg.com/200/100/any" alt="product.name" /></p>
		<p class="price">{{ product.price }}</p>
		<p class="price">{{ product.company }}</p>
	</li>
</template>
<script>
export default {
	name: "product-item",
	props: {
		product: Object,
	},
};
</script>
<style scoped>
li {
	border: 5px solid salmon;
}
.title {
	font-size: 24px;
	color: black;
	font-weight: bold;
}
</style>
