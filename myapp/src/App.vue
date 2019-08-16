<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <Navbar />
    <AllFriends :friends="friends" @delete="deleteFriend"/>
    <OnlineFriends :friends="friends" />
  </div>
</template>

<script>
import Navbar from "./Navbar";
import AllFriends from "./AllFriends";
import OnlineFriends from "./OnlineFriends";


export default {
  name: 'app',
  components: {
    Navbar,
    AllFriends,
    OnlineFriends
  },
  data () {
    return {
      msg: 'Welcome to Mukundas Vue.js App',
      friends: [
                { name:'Namrata', online: true },
                { name:'Mukunda', online: false },
                { name:'Modi', online: true },
                { name:'Ram', online: false },
            ]
    }
  },
  methods: {
    deleteFriend(payload) {
      console.log(payload)
      this.friends = this.friends.filter(friend => {
        return friend.name !== payload.name
      })
    }
  }
}
</script>

<style>
h1 {
  font-weight: normal;
  text-align: center;
}
</style>
