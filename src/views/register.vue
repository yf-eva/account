<template>
	<div class="register" :style="registerBg">
		<div class="mask"></div>
		<div class="content">
			<h1>还是注册一下吧</h1>
			<hr class="divider">
			<mt-field label="用户名" placeholder="请输入用户名" v-model="username"></mt-field>
			<hr class="divider">
			<mt-field label="手机号" placeholder="请输入手机号" v-model="phone"></mt-field>
			<hr class="divider">
			<mt-field label="密码" placeholder="请输入密码" v-model="pass"></mt-field>
			<hr class="divider">
			<mt-field label="确认密码" placeholder="请再次输入密码" v-model="checkpass"></mt-field>
			<hr class="divider">
			<mt-button type="primary">注册</mt-button>
			<div class="link">
				<mt-cell title="哎,已经注册过了的,立即登录!" :to="{name:'login'}" class="toLog"></mt-cell>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name:'register',
		data() {
			return {
				registerBg:{
					backgroundImage:'url('+require("../assets/images/bg3.jpg")+')',
					backgroundRepeat:'no-repeat',
					backgroundPosition:'center',
					backgroundSize:'100%',
					height:'',
				},
				username:'',
				phone:'',
				pass:'',
				checkpass:'',
			}
		},
		created(){
			window.screenHeight = window.innerHeight
			this.registerBg.height = window.screenHeight+'px';
			console.log(this.registerBg.height)
		},
	}
</script>

<style lang="scss">
	.register{
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
			.toLog{
				background-color: transparent;
				float: right;
				color: #67C23A;
			}
		}
	}
</style>
