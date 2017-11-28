<template>
	<div>
       <Headss/>
	   <div class="warp">
		<div class="chat">

			<div class="contact2">
				<img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/chat8.png">
				<p>您好</p>
			</div>


			<div class="contact">
				<img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/chat9.png">
				<p>你好</p>
			</div>
			
		</div>

		
		<div class="footer">
			<div class="anniu">
				<img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/chat6.png">
				<span>|</span>
				<img src="http://mraur.oss-cn-beijing.aliyuncs.com/img/chat7.png">
				<input type="text" name="" placeholder="请输入文字">
				<button>发送</button>
			</div>
		</div>
		</div>
	</div>
</template>

<script>
import Headss from '../../common/Headss'
	export default {
	  name: 'airlines',
	  data () {
	    return {
	    	
	    }
	  },
	  components:{
  	   Headss
     }

	}
</script>

<style scoped lang="less">


.warp{
	margin-top: -130/50rem;
	height: 850/70rem;
	background-color: #fff;
.chat{
	.contact{
		width:94%;
		height:40/50rem;
		margin:0 auto;
		&>img{
		width:40/50rem;
		height:40/50rem;
		}
		&>p{
			display:inline-block;
			text-align:center;
			width:67/50rem;
			line-height:25/50rem;
			background:url(http://mraur.oss-cn-beijing.aliyuncs.com/img/chat3.png) no-repeat;
			background-size:67/50rem 25/50rem;

		}
	}
	.contact2{
		width:94%;
		height:40/50rem;
		margin:34/50rem auto;
		&>img{
		width:40/50rem;
		height:40/50rem;
		float:right;
		}
		&>p{
			display:inline-block;
			text-align:center;
			width:67/50rem;
			line-height:25/50rem;
			background:url(http://mraur.oss-cn-beijing.aliyuncs.com/img/chat5.png) no-repeat;
			background-size:67/50rem 25/50rem;
			float:right;

		}

	}
	
}


.footer{
	width:100%;
	height:44/50rem;
	position: fixed;
	bottom:0;
	font-size:9/50rem;
	color:#ccc;
	.anniu{
		width:96%;
		margin-top:11/50rem;
		line-height:23/50rem;
		margin:0 auto;
		&>img{
			width:17/50rem;
			height:17/50rem;
			display:inline-block;
			margin-top:5/50rem;
		}
		&>span{
			display:inline-block;
			line-height:17/50rem;
		}
		&>input{
				width:214/50rem;
				height:23/50rem;
				border-radius:6px;
				border:2px solid #ccc;
			}
		&>button{
			width:54/50rem;
			height:25/50rem;
			border:2px solid #ccc;
			border-radius:6px;
			background:#fff;
		}
	}
}
}
</style>