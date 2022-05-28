<template>
<div>
  <h1>Witaj w systemie do zapisow na zajeciach</h1>
     <div v-if="!email">
    <login-form @login="enter($event)" button-label="Wejdź"></login-form>

  </div>

  <div v-else>
      <log-out-form : email="email"></log-out-form>
  </div>

</div>

</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
import LogOutForm from "./LogOutForm";
export default {
components: {LoginForm, LogOutForm},
data(){
  return{
     email:'',
     loggedIn:false,
  };
},
methods: {
 logMeIn(username){
 this.email=username;
 },
 logOut(){
    this.loggedIn=false;
    this.email=false;
    }
  }
}
</script>

<style>

</style>
