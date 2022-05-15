<template>
    <div id="app">
   <div id="total">
     <div id="topbox">
                <div id="title">Talking</div>
                <div id="searchdiv">
                    <span>
                        <input type="text" id="searchinput" placeholder="搜索帖子">
                        <button id="searchbutton">搜索</button>
                    </span>
                </div>
            </div>
            <div id="navi">
                <nav>
                    <router-link to="/">帖子</router-link> 
                    <router-link to="/discussion">讨论</router-link> 
                    <router-link to="/course">课程推荐</router-link> 
                    <router-link to="/question">刷题</router-link> 
                    <router-link to="/around">校园周边</router-link> 
                    <router-link to="/resource">资源共享</router-link>
                </nav>
            </div>
            <div id="bottombox">
                <div id="maincontent">
                  <div>
                    这里是帖子的内容
                  </div>
                </div>
                <div id="usercenter">
                    <div>
                      这里是用户中心
                    </div>
                </div>
            </div>
   </div>
 </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100%;
  border: 0;
  margin: auto;
}
nav {
  /* display: table-cell; */
  height: 44px;
  background-color: #ffffff;
  border-radius: 10px;
  vertical-align: middle;
  display: inline-block;
}

nav a {
  font-weight: bold;
  font-size: 20px;
  color: #2c3e50;
  width: 200px;
  /* height: 20px;
  line-height: 20px; */
  padding-top: 6px;
  vertical-align: middle;
  display: inline-block;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #42b983;
  text-decoration: none;
}

div{
  display: block;
}
body,html{
  background-color: #f5f5f5;
}
#total{
  margin-left: -20px;
  margin-top: -10px;
}
#topbox{
  /* height: 230px; */
  background-color: rgb(255, 255, 255);
  background: url("../static/background.jpg") no-repeat;
  background-size: 100%;
}
@font-face {
  font-family: 'Pattaya';
  src: url("../static/Pattaya-Regular-2.ttf");
}
#title{
  padding: 80px;
  font-size: 50px;
  font-family:'Pattaya';
  color: #fff;
}
#searchdiv{
  margin-bottom: 20px;
  font-size: 20px;
  padding-bottom: 50px;
}
#searchdiv #searchinput{
  height: 30px;
  width: 500px;
  border-radius: 15px;
  font-size: 16px;
  outline: none;
  border: 0;
}
#searchdiv #searchbutton{
  height: 30px;
  width: 70px;
  border-radius: 15px;
  font-size: 16px;
  outline: none; 
  border: 0;
  background-color: #42b983;
  color: #fff;
}
#searchdiv #searchbutton:hover{
  background: #299464;
}
#bottombox{
  display: flex;
  margin-top: 15px;
  margin-left: 300px;
  margin-right: 200px;
  border-radius: 5px;
}
#maincontent{
  width: 600px;
  background-color: #ffffff;
}
#usercenter{
  width: 200px;
  margin-left: 20px;
  background-color: #ffffff;
}
</style>
