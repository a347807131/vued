<template>
  <div id="app">
      <el-container>
          <el-header>Header</el-header>
          <el-main>
              <el-button type="primary" icon="el-icon-share"
                         v-on:click="windowOpen"
              ></el-button>
              <a href="https://baidu.com" target="_top">点击</a>
<!--              <img alt="Vue logo" src="./assets/logo.png">-->
<!--              <iframe name="Iframe1" height="400px"-->
<!--                      src="https://open.weixin.qq.com/connect/qrconnect?appid=wxfbc6ce790687f4f8&redirect_uri=http://www.msqdigital.com/portal_cstz.html&response_type=code&scope=snsapi_login&state=STATE#wechat_redirect"/>-->
              <el-row>
                  <el-col :span="8">
                      <el-tabs v-model="activeName" @tab-click="handleClick">
                          <el-tab-pane label="账户登录" name="first"></el-tab-pane>
                          <el-tab-pane label="微信登录" name="second">
                              <iframe name="Iframe1" height="400px"
                                      src="https://open.weixin.qq.com/connect/qrconnect?appid=wxfbc6ce790687f4f8&redirect_uri=http://www.msqdigital.com/portal_cstz.html&response_type=code&scope=snsapi_login&state=STATE#wechat_redirect"/>
                              <iframe name="Iframe1" height="400px"
                                      src="https://github.com/login?client_id=4bceac0b4d39cf045157&return_to=%2Flogin%2Foauth%2Fauthorize%3Fclient_id%3D4bceac0b4d39cf045157%26redirect_uri%3Dhttps%253A%252F%252Fpassport.csdn.net%252Faccount%252Flogin%253FpcAuthType%253Dgithub%2526newAuth%253Dtrue%2526state%253Dtest"/>
                          </el-tab-pane>
                      </el-tabs>
                  </el-col>
              </el-row>
          </el-main>
          <el-footer>Footer</el-footer>
      </el-container>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {

  },

    methods:{
      windowOpen(){
          window.open ('https://baidu.com','newwindow','height=100,width=400,top=0,left=0,toolbar=no,menubar=no,scrollbars=no, resizable=no,location=no, status=no')
      }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
}
</style>
