<template>
   <div>
       <label>email</label>
       <input type="email" v-model="email">
       <button @click="enter()">{{ buttonLabelToDisplay }}</button>
   </div>
</template>

<script>
export default {
 data() {
     return {
		 email: ''
     }
 },
 methods: {
     enter() {
         this.$emit('login', this.email);
     }
 },
computed: {
  buttonLabelToDisplay() {
    return this.buttonLabel || 'Zaloguj';  
  }
}
}
</script>

<style scoped>
</style>