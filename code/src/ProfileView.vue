<template>
  <head>
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
  </head>
  <title>个人主页</title> 

  <div class="common-layout">
    <el-container>
      <el-header class="header">
        <div class="header-left-icon left">
            <a class="header-link" href="#">
                <i class="fa fa-github" aria-hidden="true" style="font-size: 37.5px; color: white;"></i>    
            </a>
        </div>

        <div class="input-box left" >
            <input type="text" class="input-box-input" placeholder="搜索或跳转至">
            <img src="https://github.githubassets.com/images/search-key-slash.svg" alt="" class="input-img">
        </div>

        <!-- 头部菜单 -->
        <div class="header-menu">
            <ul>
                <li class="header-menu-li"><a href="#">Pull requests</a></li>
                <li class="header-menu-li"><a href="#">Issues</a></li>
                <li class="header-menu-li"><a href="#">Marketplace</a></li>
                <li class="header-menu-li"><a href="#">Explore</a></li>
           </ul>   
        </div>
        
        <!-- 头部右边 -->
        <div class="header-right font-normal">
            <ul>
                <li><a href="#" class="header-right-icon">
                    <i class="fa fa-bell-o"  aria-hidden="true" ></i>
                </a></li>

                <li><a href="#" class="header-right-plus">
                    <el-icon><Plus /></el-icon>
                </a></li>

                <li><a href="#" class="header-right-triangle">
                    <i class="fa fa-caret-down" aria-hidden="true"></i>
                </a></li>

                <li><a href="#">
                    <img src="https://avatars.githubusercontent.com/u/89237121?v=4" class="user-img" >
                </a></li>   

                <li><a href="#" class="header-right-triangle">
                    <i class="fa fa-caret-down" aria-hidden="true"></i>
                </a></li>
            </ul>
        </div>
      </el-header>

      <el-container>
        <el-aside width="350px">
            <!--个人信息-->
            <div class="basicInfo" style="margin-top: 20px">
                <el-row>
                    <el-col :span="12">
                        <div class="demo-basic--circle">
                            <div class="avatarImg">
                                <el-avatar :size="250" :src="circleUrl"></el-avatar>
                            </div>
                        </div>
                    </el-col> 

                </el-row>

                <el-row>
                    <el-col :span="24">
                        <div class = "userInfo">
                            <h3 style="margin-top: 50px">用户名称 (User Name):XXXX</h3>
                            <h3 style="margin-top: 20px">用户ID (User ID):xxxxx</h3>
                        </div>
                    </el-col>
                </el-row>
            </div>

            <div style="margin-top: 50px">
                <button type="button" class="editButton">
                    修改个人资料
                </button>
            </div>
        </el-aside>

        <el-container>
          <el-main>
              <div class="block text-center" style="margin-top: 20px">
                    <h3 class="hotTags">近期热门话题一览</h3>
                    <el-carousel height="150px">
                        <el-carousel-item v-for="item in 4" :key="item">
                            <h3 class="small justify-center" text="2xl">{{ item }}</h3>
                        </el-carousel-item>
                    </el-carousel>
              </div>

              <div class="createCenter" style="margin-top: 50px">
                <h2 class="sectionTitle">创作中心</h2>

                <ol class="publishList">
                    <div class="content-box d-flex width-full">
                        <div class="d-flex width-full flex-items-center position-relative">
                            <a href="undefine_link" class="text-bold flex-auto min-width-0">
                                <span class="repo" title="GitHub-20373420">帖子标题</span>
                            </a>
                            <span class="Label" style="text-align: left">发表时间</span>
                        </div>
                    </div>
                </ol>
              </div>

              <div>
                <button type="button" class="exploreButton">
                    探索发现
                </button>
              </div>
          </el-main>

          <el-footer class="footer">
            <div class="footer-left">
                
                <span style="font-size: 12px">© 2022 Talking学习生活论坛, Inc.</span>
            </div >
            <!-- <div class="footer-second"> -->
            <div class="footer-right">
                <ul>
                    <li><a href="#">隐私政策</a></li>
                    <li><a href="#">帮助</a></li>
                    <li><a href="#">联系我们</a></li>
                </ul>
            </div>
            <div class="footer-right">
                <ul>
                    <li><a href="#">API</a></li>
                    <li><a href="#">网站状态</a></li>
                    <li><a href="#">安全政策</a></li>
                </ul>
            </div>
          </el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
  
</template>

<script>
export default {
  methods: {
    imgErrHandler() {
      return true
    }
  },
  data () {
    return {
      circleUrl:"https://avatars.githubusercontent.com/u/89237121?v=4",
      sizeList: ["large", "medium", "small"]
    }
  }
}
</script>

<style scoped>
* {
    padding: 0px;
    margin: 0px;
    box-sizing: border-box;
}
body {
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji";
    font-size: 14px;
    line-height: 1.5;
    color: #24292e;
    background-color: #fff;
    min-width: 1080px;
}
p {
    margin-top: 0;
    margin-bottom: 10px;
    /* background-color: #24292f; */
}

li {
    list-style: none;
}

a{
    text-decoration: none;
    font-weight: 500;
    color: #0d66d6;
}

.left{
    float: left;
}

.right{
    float: right;
}

button,input{
    outline: none;
    background-color: none;
    border: none;
}
.header{
    width: 100%;
    height: 53px;
    background-color: #24292e;
    box-sizing: border-box;
    overflow: hidden;
    z-index: 32;
    min-width: 1025px;
    padding: 16px;
}

/* 头部icon */
.header-left-icon{
    box-sizing: border-box;
    width: 32px;
    height: 53px;
    margin-top: -4px;
    margin-left: 10px;
}

.header-link{
    font-weight: 600;
}

/* 头部输入框 */
.input-box{
    box-shadow: none;
    /* margin-top: -40px; */
    margin-left: 20px;
    min-height: 33px;
    border: 1px;
    width: 330px;
    
    height: 32px;
    margin-top: -3px;
    
}

.input-box-input{
    background-color: #3f4448;
    width: 298px;
    border-radius: 5px;
    line-height: 31px;
    padding-left: 10px;
    float: left;
    color: white;
}
.input-box-input::placeholder {
    color: hsla(0, 0%, 100%, .7);
    font-size: 14px;
    font-weight: 400;
    
}

.input-img{
    /* position: relative; */
    margin-top:  7px;
    margin-left: -30px;
    
}
/* 头部菜单 */
.header-menu{
    width: auto;
    height: auto;
    background-color: #0d66d6;
    
}
.header-menu-li a {
    float: left;
    font-weight: 600;
    color: #fff;
    font-size: 14px;
    font-family: -apple-system,BlinkMacSystemFont,Segoe UI,Helvetica,Arial,sans-serif,Apple Color Emoji,Segoe UI Emoji;
    margin: 0 16px 0 0;
    /* padding: 16px 0; */
    float: left;
}

/* 头部右边 */
.header-right{
    float: right;
    width: 150px;
    height: 32px;
    /* font-size: 17px; */
    margin: 0 2px 0 0;
    padding: 16px 2px;

}

.header-right-icon{
    box-sizing: border-box;
    color: white;
    float: left;
    font-size: 17px;
    margin-top: -16px;
}

.header-right-plus{
    box-sizing: border-box;
    float: left;
    color: white;
    font-size: 15px;
    margin-left: 20px;
    margin-top: -13px;
}

.header-right-triangle{
    box-sizing: border-box;
    float: left;
    color: white;
    font-size: 15px;
    margin-top: -14px;
    margin-left: 10px;
}

.user-img{
    height: 20px;
    width: 20px;
    border-radius:50% ;
    margin-top: -13px;
    margin-left: 30px;
    float: left;
    /* color: white; */
}

/* 页面 */


/*  左边输入框 */
.center-left-input{
    border: 1px solid #e1e4e8;
    padding: 1px 9px;
    border-radius: 5px;
}
.input-find{
    border-radius: 5px;
    width: 190px;
    height: 29px;
    padding: 5px 12px;
}

.editButton {
    position: relative;
    width: 160px;
    height: 44px;
    cursor: pointer;
    margin-top: 5px;
    display: inline-block;
    padding: 3px 12px;
    font-size: 16px;
    line-height: 20px;
    border-style: solid;
    border-width: 2px;
    border-top-color: black;
    border-right-color:black;
    border-bottom-color: black;
    border-left-color: black;
    box-shadow: 0 1px 0 rgba(27,31,35,.1), inset 0 1px 0 hsla(0,0%,100%,.03);
    background-color: #fff;
    border-radius: 24px;
    color: black;
}

.exploreButton {
    position: relative;
    width: 160px;
    height: 44px;
    cursor: pointer;
    margin-top: 5px;
    display: inline-block;
    padding: 3px 12px;
    font-size: 24px;
    line-height: 20px;
    border-style: solid;
    border-width: 2px;
    border-top-color: rgba(27, 31, 35, 0.15);
    border-right-color: rgba(27, 31, 35, 0.15);
    border-bottom-color: rgba(27, 31, 35, 0.15);
    border-left-color: rgba(27, 31, 35, 0.15);
    box-shadow: 0 1px 0 rgba(27,31,35,.1), inset 0 1px 0 hsla(0,0%,100%,.03);
    background-color: #fff;
    border-radius: 24px;
    color: #0366d6;
}

.demonstration {
  color: var(--el-text-color-secondary);
}

.el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
  text-align: center;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

/* footer */
.footer{
    /* width: 606px; */
    height: 140px;
    /* background-color: lightblue; */
    /* margin:15px 25px; */
    border: 1px;
    /* float: left; */
    margin: 0 auto;
    margin-top: 294px;
    /* max-width:700px ; */
    min-width: 520px;
}
.footer-second{
    float: left;
    margin-left: 50px;
}
.footer-left{
    /* background-color: black;
    margin: 0 32px 0 0; */
    width: 172px;
    height: 128px;
    float: left;
    position: relative;
    color: #c7cbd1;
}

.footer-right{
    /* background-color: rgb(49, 47, 47); */
    width: 80px;
    height: 128px;
    float: right;
    position: relative;
    /* padding: 0 0 0 24px; */
    /* box-sizing: border-box; */
    margin-left:24px;
}
.footer-right a{
    color: #586069;
}


h2 {
  text-align: left;
}

ol {
    display: block;
    list-style-type: decimal;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-inline-start: 40px;
}
.d-flex {
    display: flex !important;
}
.width-full {
    width: 100% !important;
}
.demo-basic--circle{
    position:relative;  /* 设置为绝对定位，使下方的top和left生效  */
    top: 5%;
    left: 25%;
    bottom: 5%;
}
.content-box {
    width: 300px;
    padding: 40px;  /* 内边界宽度  */
    box-sizing: border-box;
    background-color: var(--color-canvas-default);
    border-color: var(--color-border-default);
    border-style: solid;
    text-align: center;  /* 表单中内容居中  */
    border-radius: 10px;
}

</style>