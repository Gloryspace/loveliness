<template>
	<div class="vessel">
		<Headss/>
		<div class="warp">
		<div class="subject-body">
			<div class="subject-body-txt">
				<ul>
					<router-link tag='li' :to="{name:'material',query:{title:'个人资料'}}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set1.png" alt=""><a href="#">个人资料</a></router-link>
					<router-link tag='li' :to="{path:'/bindphone'}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set2.png" alt=""><a href="#">绑定</a></router-link>
					<router-link tag='li' :to="{name:'address',query:{title:'收货地址'}}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set3.png" alt=""><a href="#">收货地址</a></router-link>
					<li><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set4.png" alt=""><a href="#">清除缓存</a></li>
					<li>
						<img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set5.png" alt="">
						<a href="#">小屏模式（省高达70%流量）</a>
						<el-tooltip :content="''" placement="" class="switch">
							  <el-switch v-model="value5" active-color="#13ce66" inactive-color="#ff4949"
							    active-value="100" inactive-value="0">
							  </el-switch>
						</el-tooltip>

					</li>
					<li><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set6.png" alt=""><a href="#">消息推送</a></li>
					<router-link tag='li' :to="{path:'/abouts'}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set7.png" alt=""><a href="#">关于loveliness</a></router-link>
					<router-link tag='li' :to="{name:'help',query:{title:'帮助'}}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set8.png" alt=""><a href="#">帮助</a></router-link>
					<router-link tag='li' :to="{name:'airlines',query:{title:'loveliness客服'}}"><img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/set9.png" alt=""><a href="#">意见反馈</a></router-link>
				</ul>
			</div>
			<router-link tag='button' :to="{path:'/logins'}" type="button">退出登录</router-link>
		</div>
		</div>
	</div>
</template>
<script>
import Headss from '../common/Headss'
export default {
  name: 'setting',
  data(){
  	return{
  		 value5: '100'
	}
  },
   components:{
  	Headss
  }
}
</script>
<style scoped lang="less">
.vessel{
		width: 100%;
		margin: 0 auto;
		.warp{
			width:100%;
			background-color: #fff;
            height: 667/50rem;
		}
		.subject-body{
			width: 358/50rem;
			height: 600/50rem;
			background: #fff;
			margin: -90/50rem auto;
			background-color: #fff;
			border-radius: 5/50rem;
			box-shadow:0px 0px 5px 1px #bbb;
			text-align: center;
			.subject-body-txt{
				text-align: left;
				font-size: 14/50rem;
				font-family:宋体;
				color: #4D4D4D;
				position: relative;
				top: 23/50rem;
				ul{
					li{
						height: 26/50rem;
						margin-bottom: 24/50rem;
						margin-left: 15/50rem;
						position: relative;
						&>.el-switch{
							line-height: 10px;
							position: absolute;
							right:20/50rem;
							top:0.1rem;
						}
						img{
							margin-right: 8/50rem;
							width: 19/50rem;
							height: 19/50rem;
							position: relative;
							top: 4.5/50rem;
						}
					}
				}
			}
			button{
				width: 277/50rem;
				height: 42/50rem;
				border-radius: 10/50rem;
				border: none;
				background: #fff;
				margin-top: 23/50rem;
				box-shadow:0px 0px 20px 2px #ccc;
				font-size:14/50rem;
				outline:none;
			} 
		}
	}
</style>
