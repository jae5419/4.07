<template>
  <div>
    <span>아이디</span>
    <input type="text" v-model="user">
    <br>
    <span>패스워드</span>
    <input type="password">
    <br>
    <button @click="login">로그인</button>
    <button @click="$router.push('/')">취소</button>
  </div>
</template>

<script>
export default {
  name: "LoginView",
  data: () => ({
    user: ""
  }),
  methods: {
    login: function() {
      this.$emit('login', this.user);
      this.$router.push('/');
    }
  }
}
</script>
