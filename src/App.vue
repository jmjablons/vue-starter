<template>
<div>
<h1>System zapisów</h1>
<div v-if="isAuthenticated">
	<p> Logged as {{ email }}</p>
	<button @click="logMeOut()">Sign out</button>
	</div>
<div v-else>
	<input type ="text" v-model="email">
	<button @click="logMeIn()">Sign in</button>
	</div>
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
