<template>
	<div class="home" :style="homeBg">
		<div class="mask"></div>
		<div class="btn content">
			<mt-button plain @click.native="toLogin">登录</mt-button>
			<mt-button plain @click.native="toRegister">注册</mt-button>
		</div>
		
	</div>
</template>

<script>
	export default {
		name:'home',
		data() {
			return {
				homeBg:{
					backgroundImage:'url('+require("../assets/images/bg0.jpg")+')',
					backgroundRepeat:'no-repeat',
					backgroundPosition:'center',
					backgroundSize:'120%',
					height:'',
				},
				
			}
		},
		created(){
			window.screenHeight = window.innerHeight
			this.homeBg.height = window.screenHeight+'px';
			console.log(this.homeBg.height)
		},
		methods:{
			toLogin(){
				this.$router.push({path:'/login'})
			},
			toRegister(){
				this.$router.push({path:'/register'})
			}
		}
	}
</script>

<style lang="scss">
	.home{
		width: 100%;
		position: relative;
		.btn{
			position: absolute;
			top:62%;
			
			 .mint-button{
				 width: 80px;
				 border:1px solid #fff;
				 color: #fff !important;
				 margin: 0 10px;
				 background: radial-gradient(circle,#53A8FF,#D9ECFF);
			 }
		}
	}
</style>
