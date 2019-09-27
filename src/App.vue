<template>
<div id="app">
<!-- <img alt="Vue logo" src="./assets/logo.png"> -->
<h2>System do zapisow</h2>
<!-- <p>Podaj email</p>
<input type="email" v-model="email"> -->
  <!-- <span v-bind:title="message">
    Hover your mouse over me for a few seconds
    to see my dynamically bound title!
  </span> -->
<!-- <button @click="logIn()">Sign in</button> -->
<!-- <button v-on:click="count++">You clicked me {{ count }} times.</button> -->
<login-form @login="logMeIn($event)"></login-form>
<login-form @login="enter($event)" :button-label="'WejdŸ'"></login-form>
<meetings-page></meetings-page>
</div>
</template>

<script>
import "milligram";
import LoginForm from "./components/LoginForm";
import MeetingPage from "./components/MeetingPage";
import NewMeetingForm from "./components/NewMeetingForm";
import MeetingList from "./components/MeetingList";
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    LoginForm,
    MeetingPage
    // HelloWorld
    },
    data() {
      return {
        email: '',
        count: 0,
        message: 'You loaded this page on ' + new Date().toLocaleString()
      }
    },
  methods: {
  alertMyEmail() {
    alert(this.email);
    },
  logIn(){ 
    this.$emit('login', this.email);
  },
  logMeIn(username) {
  this.authenticatedUsername = username;
}
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
