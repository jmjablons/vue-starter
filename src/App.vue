<template>
<div>
<h1>System zapisów</h1>
<div v-if="isAuthenticated">
	<p> Logged as {{ email }}</p>
	<button @click="logMeOut()">Sign out</button>
	</div>
<div v-else>
	<login-form @login="logMeIn($event)">Sign in</login-form>
	</div>
	</div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
export default {
	components: {LoginForm},
	data() {
		return {
			email: '',
			isAuthenticated: false
		}
	},
	methods: {
		logMeIn(username){
			this.email =  username;
			this.isAuthenticated = true; 
		},
		enter(){
			this.$emit
		},
		logMeOut(username){
			this.email =  '';
			this.isAuthenticated = false; 
		}
		}
}

</script>

<style>
</style>
