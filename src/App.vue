<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
	*{
		margin:0;
		padding:0;
	}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
	position: relative;
}
.mask{
	width: 100%;
	height: 100%;
	opacity: .6;
	background-color: #fff;
}
.content{
	position: absolute;top:0;left: 0;
	width: 100%;
}
.divider{
	display: block;
	width:90%;
	margin: 0 auto;
	border-color: #ECF5FF;
}
h1{
			margin: 150px 0 50px;
			background:linear-gradient(to bottom, #409EFF, #D9ECFF);
			-webkit-background-clip: text;
			color: transparent;    
		}
</style>
