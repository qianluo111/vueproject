<template>
  <div class="foot">
    <div class="school">
      <div class="sch-header">
        <img src="@/assets/img/shouye/国际航空服务与管理_99.jpg" alt="" />
      </div>
      <div class="sch-content">
        <div class="sch-colleage">
          <img src="@/assets/img/公共/首页改1_40.gif" alt="" />
          <span>北京市航空中学</span>
        </div>
        <div class="sch-colleage">
          <img src="@/assets/img/公共/首页改1_37.gif" alt="" />
          <span>吉林大学</span>
        </div>
        <div class="sch-colleage" style="margin: 0.08rem 0">
          <img src="@/assets/img/公共/首页改1_44.gif" alt="" />
          <span>大连海事大学</span>
        </div>
        <div class="sch-colleage" style="margin: 0.08rem 0">
          <img src="@/assets/img/公共/首页改1_46.gif" alt="" />
          <span>渤海大学</span>
        </div>
        <div class="sch-colleage">
          <img src="@/assets/img/公共/首页改1_50.gif" alt="" />
          <span>山东杏林航空大学</span>
        </div>
        <div class="sch-colleage">
          <img src="@/assets/img/公共/首页改1_52.gif" alt="" />
          <span>南京市航空大学</span>
        </div>
      </div>
      <div class="information_con_btm">
          <div class="btm_border">
              <span>查看更多问题</span>
              <img src="@/assets/img/公共/sou.png" alt="">
          </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
   
  },
};
</script>
<style lang='scss' scoped>

.school {
  width: 3.54rem;
  min-height: 1rem;
  background: #fff;
  margin: 0.15rem auto 0;
  border-radius: .05rem .05rem 0 0;
  overflow: hidden;
  padding-bottom: 0.01rem;
  border-bottom-right-radius: 0.04rem;
  border-bottom-left-radius: 0.04rem;
  .sch-header {
    width: 100%;
    height: 0.55rem;
    img {
      width: 100%;
    }
  }
  .sch-content {
    width: 100%;
    min-height: 1rem;
    background: #fff;
    margin-top: 0.1rem;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    .sch-colleage {
      width: 1.65rem;
      height: 0.55rem;
      border-radius: 0.06rem;
      padding: 0.05rem 0 0.05rem 0.05rem;
      display: flex;
      align-items: center;
      border: 0.01rem solid #ccc;
      border-radius: 0.06rem;
      img {
        width: 0.5rem;
        height: 0.5rem;
      }
      span {
        font-size: 0.14rem;
        flex: 1;
        padding: 0 0 0 .1rem;
        color: rgb(102, 102, 102);
      }
    }
  }
   .information_con_btm{
      padding: .15rem .12rem .25rem .12rem;
      .btm_border{
          width: 100%;
          height: 100%;
          border-radius: 5px;
          border: solid 1px #1776af;
          text-align: center;
          line-height: .42rem;
          span{
              font-size: .16rem;
              color: #1776af;
              font-family: PingFang-SC-Medium;
              font-weight: normal; 
              font-stretch: normal;
              letter-spacing: 0px;
          }
          img{
              width: 0.16rem;
              height: 0.16rem;
              margin-left: .04rem; 
              vertical-align: middle;
              margin-bottom: .02rem;   
          }
      }
      :hover{
          background: #3f555f;
      }
      :hover>span{
          color: #ffffff;
          font-size: .16rem;
          font-family: PingFang-SC-Medium;
          font-weight: normal; 
          font-stretch: normal;
          letter-spacing: 0px;
      }
  }
}

</style>
