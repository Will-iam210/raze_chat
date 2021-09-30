<!--William-->
<template>
  <div class="login-container">
    <button @click="loginSubmit">Login with Google</button>
  </div>
</template>

<script>
import firebase from "firebase/compat";
export default {
  methods: {
    loginSubmit() {
      const provider = new firebase.auth.GoogleAuthProvider()
      firebase.auth().signInWithRedirect(provider)
          .catch(console.log)
    }
  }
}
</script>
<!--William-->

<style>
/*Leonardo*/
.login-container {
  width: 100%;
  text-align: center;
  padding-top: 50px;
}
.login-container button {
  width: 30%;
  background-color: #4e37fc;
  color: white;
  font-weight: bold;
  font-size: 18pt;
  /*Leonardo*/
  /*Jesus*/
  padding: 20px;
  border-radius: 15px;
  border: none;
  box-shadow: #00004040 0px 5px 10px;
  cursor: pointer;
}

.login-container button:hover {
  background-color: #7562ff;
}
/*Jesus*/

</style>