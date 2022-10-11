<template>
	<div class="container">
		<h1>Aquí estará lo proveniente de javascript</h1>

		<ul>
			<li>{{ suma(2, 2) }}</li>
			<li>{{ saludar("Carlos") }}</li>
			<li>Elements below will be displayed if pass a condition!!</li>
			<li><button @click="show()">Clickme for show or hide!</button></li>
			<li v-if="isRender">If condition is true, will display this content</li>
			<li v-else>Else the content displayed will be this</li>
			<li v-show="isRender">
				If the condition is true, will display this with V_SHOW
			</li>
		</ul>
	</div>
</template>
<script setup>
import { ref } from "vue";
const suma = (a, b) => {
	return `la suma de ${a}+${b}=${a + b}`;
};
const saludar = (name) => `Hello ${name}, wellcome home!`;
let isRender = ref(false);
const show = () => {
	isRender.value = !isRender.value;
};
</script>
<style scoped>
.container {
	display: flex;
	justify-content: center;
	flex-direction: column;
	align-items: center;
	background-color: aqua;
}
ul {
	display: flex;
	flex-direction: column;
	background-color: aquamarine;
}
</style>
