<template>
  <div id="app">
	  <keep-alive>
		  <router-view></router-view>
	  </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App',
  mounted() {
	  this.$router.push({
		  path: "/home"
	  })
  }
}
</script>

<style>
	body {
		margin: 0;
	}
</style>
