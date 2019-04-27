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
