<template>
  <div class="shop-video">
    <div class="video-body" v-for="(item,key) in newsList">
      <div class="video-txt">
        <img :src="item.headimg" alt="">
        <p>{{item.name}}</p>
        <p>{{item.time}}</p>
      </div>
      <div class="video-top">
        <img :src="item.img" alt="">
      </div>
    </div>
    <p class="text">到位啦</p>
  </div>
</template>
<script>
	export default{
		name:'collectmovie',
		data(){
			return{
      newsList:{}
			}
		},
    created(){
      this.$axios.get('./static/json/three.json')
     .then(res => {
     this.newsList=res.data.video
     })
    .catch(error => {
      console.log(error)
    })
   },
	}
</script>
<style scoped lang="less">
  .shop-video{
    width: 100%; 
    color:#C6C6C6;
    text-align: center;
    font-size: 12/50rem;
    .video-body{
      margin: 0 auto;
      width: 355/50rem;
      height: 212/50rem;
      background: #fff;
      box-shadow:0px 0px 20px 1px #ccc;
      border-radius: 10px;
      &:nth-child(2){
          margin-top: 20/50rem;
        }
      .video-txt{
        height: 38/50rem;
        width: 335/50rem;
        margin: 0 auto;

        &>img{
          width: 24/50rem;
          position: relative;
          top: 7/50rem;
          display: inline-block;
          float: left;
        }
        &>p{
          font-size: 12/50rem;
          display: block;
          float: left;
          line-height: 38/50rem;
          margin-left: 10/50rem;
           &:nth-child(3){
          float: right;
        }
        }
       
      }
      .video-top{
        width: 335/50rem;
        height: 160/50rem;
        margin: 0 auto;
        // position: relative;
        // top: 38/50rem;
        &>img{
          width: 100%;
        }
      }
    }
    .text{
      margin-top: 20/50rem;
    }
  }

</style>