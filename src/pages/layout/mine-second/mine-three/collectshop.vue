<template>
  <div class="collect-product-list">
  <Commodity/>
</div>
</template>

<script>
import Commodity from "../../find-second/find-common/commodity"
export default {
  name: 'collect',
  data(){
    return{
  }
  },
  components:{
  	Commodity
  }
}

</script>

<style scoped lang="less">
.collect-product-list{
	width: 95%;
	margin: 0 auto;
	height: 160/50rem;
	box-sizing: border-box;
	border-radius: 10px;
	&>div:nth-child(2){
		float: right;
	}
	.product-item{
		float: left;
		width:160/50rem;
		height:160/50rem;
		box-shadow:0px 0px 20px 1px #ccc;
		border-radius: 10px;
	
}
}
</style>