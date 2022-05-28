<template>
   <div>
       <label>Witaj {{email}}</label>
       <a @click="logOut()">Wyloguj</a>
     </div>
</template>

<script>

export default {
props: ['email'],

 methods: {
     logOut() {
         this.$emit('logout');
     },
 }
}
</script>