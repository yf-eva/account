<template>
	<div class="login" :style="loginBg">
		<div class="mask"></div>
		<div class="content">
			<h1>欢迎登录</h1>
			<hr class="divider">
			<mt-field label="手机号" placeholder="请输入手机号" v-model="phone"></mt-field>
			<hr class="divider">
			<mt-field label="密码" placeholder="请输入密码" v-model="pass"></mt-field>
			<hr class="divider">
			<mt-button type="primary">登录</mt-button>
			<div class="link">
				<mt-cell title="忘记密码？" :to="{name:'register'}" class="toPwd"></mt-cell>
				<mt-cell title="还没注册？" :to="{name:'register'}" class="toRsg"></mt-cell>
			</div>
			
		</div>
	</div>
</template>

<script>
	export default {
		name:'login',
		data() {
			return {
				loginBg:{//背景图
					backgroundImage:'url('+require("../assets/images/bg1.jpg")+')',
					backgroundRepeat:'no-repeat',
					backgroundPosition:'center',
					backgroundSize:'100%',
					height:'',
				},
				phone:'',
				pass:'',
				
			}
		},
		created(){
			window.screenHeight = window.innerHeight
			this.loginBg.height = window.screenHeight+'px';
			console.log(this.loginBg.height)
		},
	}
</script>

<style lang="scss" >
	.login{
		width: 100%;
		.mint-field{
			background-color: transparent;
			color: #409EFF;
			.mint-cell-wrapper{
				.mint-cell-title{
					
				}
				.mint-field-core{
					background-color: transparent;
				}
			}
			
		}
		.mint-button{
			background: radial-gradient(circle, #409EFF, #D9ECFF);
			width:80%;
			margin-top:20px;
		}
		.link{ 
			width:100%;
			margin-top:20px; 
			.toPwd{
				background-color: transparent;
				float: left;
				color: #67C23A;
			}
			.toRsg{
				background-color: transparent;
				float: right;
				color: #67C23A;
			}
		}
	}
</style>
