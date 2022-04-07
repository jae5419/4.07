<template>
  <div>
    <h1>게시글 목록입니다</h1>
    <nav>
      <router-link to="/page/1">1</router-link> |
      <router-link to="/page/2">2</router-link> |
      <router-link to="/page/3">3</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>
