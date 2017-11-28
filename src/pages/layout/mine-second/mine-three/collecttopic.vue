<template>
  <div class="shop-topic">
   <div class="topic-list" v-for="(item,key) in newsList">
    <router-link :to="{name:'articles',query:{title:'文章'}}">
      <div class="topic-image">
        <img :src="item.img">
      </div>
    </router-link>
      <div class="user">
        <div class="user-left">
          <img :src="item.headimg">
          <p>{{item.name}}</p>
        </div>
        <div class="user-right">
          <a href="javascript:;">{{item.num}}</a>
        </div>
      </div>
   </div>
</div>
</template>

<script>
export default {
  name: 'topic',
  data(){
    return{
      newsList:{}
  }
  },
  created(){
      this.$axios.get('./static/json/three.json')
     .then(res => {
     this.newsList=res.data.collenttopic
     console.log(this.newsList);
     })
    .catch(error => {
      console.log(error)
    })
   }
}

</script>

<style scoped lang="less">
.shop-topic{
  width: 100%;
  padding: 0 10/50rem;
  box-sizing: border-box;
  .topic-list{
    margin-top: 0.1rem;
    .topic-image{
      overflow: hidden;
      box-shadow:0px 0px 20px 1px #ccc;
      &>img{
        width:355/50rem;
        hieght:3rem;
        float: left;
      }
    }
    .user{
      overflow: hidden;
      margin-top: 10/50rem;
      .user-left{
              float: left;
        width: 100px;
              &>img{
                float: left;
                width:26/50rem;
                hieght:26/50rem;
                margin-right: 10/50rem;
              }
              &>p{
                 margin-top: 7/50rem;
                 color:#c1c1c1;
              }
      }
      .user-right{
        float: right;
        &>a{
          position: relative;
          display: block;
          margin-top: 8/50rem;
          &:before{
            content: "";
            width:20/50rem;
            height:20/50rem;
            background: url(http://mraur.oss-cn-beijing.aliyuncs.com/img/topic.png);
            background-size: 20/50rem 20/50rem;
            position: absolute;
            top: -0.1rem;
            left:-0.5rem;
          }
        }
      }
    }
  }
}
</style>