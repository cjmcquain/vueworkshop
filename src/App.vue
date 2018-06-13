<template>
  <div id="app">
    <h1>Hello there {{ user.firstname }} {{ user.lastname }}!</h1>
    <h2>You're logged in as {{ user.username }}</h2>
    <h3 v-if="myBoolean">Your e-mail address is {{ user.email }}</h3>
    Username: <input type="text" v-model="user.username"><br>
    First name: <input type="text" v-model="user.firstname"><br>
    Last name: <input type="text" v-model="user.lastname"><br>
    E-mail address: <input type="text" v-model="user.email"><br>
    Myboolean is {{ myBoolean }}
    <button style="background-color: red" @click="toggleBoolean">Show my info</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {
        username: '',
        firstname: '',
        lastname: '',
        email: '',
        password: ''
      },
      myBoolean: true
    }
  },
  methods: {
    toggleBoolean() {
      this.myBoolean = !this.myBoolean
    }
  }
}
</script>

<style>

</style>
