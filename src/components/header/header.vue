<template>
  <div class="wrap actt">
    <div class="inp">
      <span class="spn">欢迎来到紧缺应用技术技能型人才职业教育报考平台</span>
    </div>
    <div class="logo_body">
        <router-link to="/" tag="div" class="logo">
          <img src="@/assets/images/首页改1_03.gif" alt="" />
        </router-link>
      <div class="menu">
        <img @click="btn()" src="@/assets/images/首页改1_05.gif" alt="" />
        <div class="txt" :class="{'act':isloading}">
          <router-link to="/" tag="p">首页</router-link>
          <router-link to="/Service" tag="p">VIP地勤专业</router-link>
          <router-link to="/hangkong" tag="p">航空学院</router-link>
          <router-link to="/hangkong/chuzhongsheng" tag="p">初中生</router-link>
          <router-link to="/hangkong/gaozhongsheng" tag="p">高中生</router-link>
          <router-link to="/hangkong/sanxiaosheng" tag="p">三校生</router-link>
          <router-link to="/hangkong/yikaosheng" tag="p">艺考生</router-link>
          <router-link to="/youlun" tag="p">游轮海城专业</router-link>
          <router-link to="/kongcheng" tag="p">空乘专业</router-link>
          <router-link to="/zhaoshengyaoqiu" tag="p">招生要求</router-link>
          <router-link to="/gaotie" tag="p">高铁乘务专业</router-link>
          <router-link to="/ynjd" tag="p">疑难解答</router-link>
        </div>
        <div class="quan" v-if="isloading" @click="btn()"></div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
 data(){
     return {
         isloading:false,
     }
 },
 methods:{
     btn(){
        if(this.isloading==true){
          this.isloading=false
        }else{
          this.isloading=true
        }
     },
     scroll(){
        if(this.isloading==true){
          this.isloading=false
        }
     }
 },
 mounted(){
     this.scrollHanle = this.scroll.bind(this)  
     window.addEventListener('scroll',this.scrollHanle)
  },
  destroyed() {
    window.removeEventListener("scroll",this.scrollHanle)
  },
 watch:{
   $route:{
     handler(){
        if(this.isloading==true){
          this.isloading=false
        }
     },
     immediate:true
   }
 },
};
</script>

<style lang="scss" scoped>
.actt{
    position: fixed;
    left: 50%;
    top: 0;
    transform: translate(-50%,0);
    z-index: 9999;
}
.inp {
  width: 3.75rem;
  margin: 0 auto;
  height: 0.3rem;
  background-color: #ffffff;
  display: flex;
  align-items: center;
  .spn {
    height: 0.12rem;
    
    font-family: PingFang-SC-Medium;
    font-size: 0.12rem;
    font-weight: normal;
    font-stretch: normal;
    letter-spacing: 0rem;
    color: #777777;
    padding-left: 0.13rem;
  }
}

.logo_body {
  width: 3.75rem;
  height: 0.49rem;
  margin: 0 auto;

  background: #eaeaea;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .logo {
    box-sizing: border-box;
    img {
      width: 1.03rem;
      height: 0.29rem;
      padding: 0.1rem 0.1rem;
    }
  }
  .menu {
    position: relative;
    padding: 0.15rem;

    img {
      width: 0.3rem;
      height: 0.22rem;
    }
    .txt{
        width: 1.5rem;
        background:#fff;
        z-index: 2;
        position: absolute;
        right: 0;
        top: .38rem;
        height: 0;
        transition: all 0.3s linear;
        z-index: 3;
        overflow: hidden;
        p{
          height: .40rem;
          text-align: center;
          line-height: .4rem;
        }
    }
    .act{
      height: 4.4rem;
    }
    .quan{
      width: 100%;
      height: 100%;
      position: fixed;
      left: 0;
      top: 0;
      opacity: 0;
      z-index: 2;
    }
  }
}


</style>