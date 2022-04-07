<template>
  <div id="app">
    <button @click="$router.push('/login')">로그인</button>
    <button v-if="loged" @click="$router.push(`/${user}`)">{{ user }}님의 정보</button>
    <button v-if="loged" @click="logout">로그아웃</button>
    <router-view @login="login" />
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    user: "",
    loged: false
  }),
  methods: {
    login: function(name) {
      this.user=name;
      this.loged=true;
    },
    logout: function() {
      this.user="";
      this.loged=false;
      this.$router.push('/');
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
