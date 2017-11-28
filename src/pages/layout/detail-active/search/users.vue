<template>
  <div class="users">
    <div class="box-mid">
      <div class="container">
        <!-- 一页展示十条数据 -->
        <div class="con" v-for="(item,idx) in newList">
          <img :src="item.img">
          <span>{{item.name}}</span>
          <a href="javascript:;">关注ta</a>
        </div>

      </div>
    </div>
  </div>
</template>

<script>



export default {
  name: 'users',
  data () {
    return {
      newList:{}
    }
  },
   created(){
      this.$axios.get('./static/json/three.json')
     .then(res => {
     this.newList=res.data.users
     })
    .catch(error => {
      console.log(error)
       })
     }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

// 25px   1rem = 50px;  0.5rem  
// 18px

// rem适合固定布局的形式
// 百分比 、 css3弹性盒子模型
.users{
  background:#fff;
  width: 100%;
  .box-mid{
    .container{

      // height:5rem;
      width:285/50rem;
      padding-left: 0.2rem;
      background:#fff;
      margin:0 auto 0.4rem;
      padding-bottom: 1px;
      .con{
        margin-bottom: 0.2rem;

        &>img{
          height:0.8rem;
          vertical-align: top;
          margin-right: 0.2rem;
        }
        &>span{
          display: inline-block;
          height: 0.8rem;
          line-height: 0.8rem;
        }
        a{
          display:inline-block;
          line-height:0.2rem;
          border-radius:0.2rem;
          border:1px solid #8c8c8c;
          padding:0.15rem;
          float:right;
          margin:0.2rem 0.2rem 0 0;
        }
      }
    }
   

  } 
}

 

</style>

