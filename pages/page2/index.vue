<template>
  <div class="container">
    <h1 class="title">
      PAGE 2
    </h1>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      title: 'OG TEST!'
    }
  }
}
</script>

<style>
.container {
  margin: 30px auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
