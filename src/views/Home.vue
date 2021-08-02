<template>
  <div class="home">
    <h1>This is an Home page</h1>
    <el-button @click="getRouter">点击</el-button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  methods: {
    getRouter () {
      this.$router.push({ path: '/about', query: { id: '2' } }).catch(() => { });
    }
  }
}
</script>
