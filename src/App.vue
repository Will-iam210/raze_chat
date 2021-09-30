
<template>
<!--Jesus-->
  <div id="app">
    <Chat v-if="user"></Chat>
    <Login v-else></Login>
  </div>
</template>
<!--Jesus-->
<script>
//Leonardo
import Chat from './components/Chat'
import Login from './components/Login'
import firebase from "firebase/compat";
export default {
  data() {
    return {
      user: firebase.auth().currentUser
    }
  },
  name: 'App',
  components: {
    Chat, Login
  }
}
//Leonardo
</script>

<style>
/*Detallitos William*/
body {
  background-color: #F7F8F3;
}
</style>