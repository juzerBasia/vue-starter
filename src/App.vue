<template>
<div>
  <h1>Witaj w systemie do zapisow na zajeciach</h1>
     <div v-if="!email">
    <login-form @login="enter($event)" button-label="Wejdź"></login-form>
    <login-form @login="enter($event)" button-label="Wleć"></login-form>
    <login-form @login="enter($event)" :button-label="Math.random() < 0.5 ? 'Etykieta A' : 'Etykieta B'"></login-form>

  </div>

  <div v-else>
   <h2>Witaj {{ email }}</h2>
   <a @click="logOut()">Wyloguj</a>
  </div>
</div>

</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";
export default {
components: {LoginForm},
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
