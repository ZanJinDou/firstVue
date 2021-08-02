<template>
  <div class="about">
    <h1>This is an about page</h1>
    <el-button @click="getRouter">点击</el-button>
  </div>
</template>
<script>

export default {
  name: 'about',
  methods: {
    getRouter () {
      this.$router.push({ path: '/' });
    }
  }
}
</script>