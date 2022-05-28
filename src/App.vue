<template>
  <div>
  <h1>Twój e-mail to {{ email }}</h1>
   <h2>Twój e-mail to {{ email }}</h2>
   {{email.length}}
  <input type="text" v-model="email">
 </div>
</template>

<script>

export default {
data(){
return{
email:'',
}}
};
</script>

<style>

</style>
