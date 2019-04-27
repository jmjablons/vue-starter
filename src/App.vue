<template>
<div>
<p>{{ email }}</p>
<input type ="text" v-model="email">
<button @click="logMeIn()">Sign in</button>
</div>
</template>

<script>
import "milligram";
export default {
	data() {
		return {
			email: '',
			isAuthenticated: false
		}
	},
	methods: {
		logMeIn(){
			this.isAuthenticated = true;
		},
		logMeOut(){
			this.isAuthenticated = false;
			this.email = ''
		}
		}
}

</script>

<style>
</style>
