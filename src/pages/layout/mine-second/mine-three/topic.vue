<template>
	<div>

		<Headss/>
        <div class="warp">
		<div class="center" v-for="(item,key) in newsList">
			<div class="content">
				<img :src="item.headimg">
				<div class="name">
					<p>{{item.txt}}</p>
				</div>
			</div>
		</div>
    </div>

		



		
	</div>
</template>

<script>
import Headss from "../../common/headss"
	export default {
	  name: 'topic',
	  data () {
	    return {
	    	newsList:{}
	    }
	  },
	  components:{
	  	Headss
	  },
	    created(){
      this.$axios.get('./static/json/three.json')
     .then(res => {
     this.newsList=res.data.topicz
     })
    .catch(error => {
      console.log(error)
    })
   }
	}
</script>

<style scoped lang="less">
.warp{
	margin-top: -100/50rem;
	background-color: #fff;
	height: 665/50rem;
}
.center{
	width:100%;
	height:78/50rem;
	border-top:1px solid #ddd;
	border-bottom:1px solid #ddd;
	margin-top:9/50rem;
	.content{
		width:329/50rem;
		height:48/50rem;
		margin:0 auto;
		margin-top:16/50rem;
		&>img{
			width:48/50rem;
			height:48/50rem;
			float:left;
		}
		.name{
			float:left;
			margin-left:9/50rem;
			&>p{
				line-height:23/50rem;
				font-size:13/50rem;
			}
		}
			
				

	}
}

</style>