<template>
  <div>
    <div class="container1">
      <b-container>
        <b-row>
          <b-col>
            <div class="logo"></div>
            <h2 class="subtitle">觅迹，轻量级室内导航解决方案</h2>
            <p>
              应用于商超、景点、园区等区域内寻路场景，结合使用场景可以扩展全局消息、商家消息、和途径消息等多样化功能。
            </p>
            <div class="links">
              <a href="#about" class="button--green">关于觅迹</a>
              <a href="https://github.com/tracesr" target="_blank" class="button--grey">GitHub</a>
            </div>
          </b-col>
          <b-col>
            <div class="mockup">
              <div class="mockup__frame"></div>
              <div class="mock_code"></div>
              <video
                autoplay="autoplay"
                loop="loop"
                muted="muted"
                playsinline
                class="mockup__video"
              >
                <source src="~static/caozuo.mp4" type="video/mp4">
              </video>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div class="container2" id="about">
        <b-container>
            <div class="tc">
                <h1 class="title">觅迹</h1>BETA
                <p class="subt">能为你提供什么</p>
            </div>
            <b-row class="featureList">
                <b-col>
                    <h2 class="_hd"><i class="ion">&#xe7c0;</i> 导航系统</h2>
                      <ul>
                          <li>
                            <i class="ion">&#xe600;</i> 基础地图
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 商家检索
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 路径规划
                          </li>
                          <li>
                            <i class="ion">&#xe62d;</i> 覆盖物标注
                          </li>
                          <li>
                            <i class="ion">&#xe62d;</i> 地图主题
                          </li>
                      </ul>
                </b-col>
                <b-col>
                    <h2 class="_hd"><i class="ion">&#xe6a5;</i> 地图编辑器</h2>
                    <ul>
                          <li>
                            <i class="ion">&#xe600;</i> 支持SVG图形导入
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 商家信息编辑
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 路径绘制
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 数据导入导出
                          </li>
                          <li>
                            <i class="ion">&#xe62d;</i> 覆盖物编辑
                          </li>
                    </ul>
                </b-col>
                <b-col>
                    <h2 class="_hd"><i class="ion">&#xe613;</i> 消息系统</h2>
                    <ul>
                          <li>
                            <i class="ion">&#xe600;</i> 全局公告
                          </li>
                          <li>
                            <i class="ion">&#xe600;</i> 商家公告
                          </li>
                          
                    </ul>
                </b-col>
                <b-col>
                    <h2 class="_hd"><i class="ion">&#xe7af;</i> 定制主页</h2>
                    <ul>
                          <li>
                            <i class="ion">&#xe62d;</i> 营销信息聚合
                          </li>
                          <li>
                            <i class="ion">&#xe62d;</i> 商户分类检索
                          </li>
                          <li>
                            <i class="ion">&#xe62d;</i> 品牌入驻
                          </li>
                    </ul>
                </b-col>
            </b-row>
            <p class="_tip">标注 <i class="ion">&#xe62d;</i> 的功能正在积极开发中</p>
        </b-container>
    </div>
    <!-- <div class="container3">
        <b-container>
            3
        </b-container>
    </div> -->
    <div class="footer">
      <b-container>
        <b-row class="_main">
          <b-col class="_links">
            <div class="_hd">About</div>
            <ul>
              <li>
                <b-badge variant="primary">Email</b-badge>
                tower1229@foxmail.com
              </li>
              <li>
                <b-badge variant="success">Website</b-badge>
                tracesr.github.io
              </li>
              <li>
                <b-badge variant="danger">Author</b-badge>
                <strong><a href="https://refined-x.com/about/" target="_blank">雅X共赏</a></strong>
              </li>
            </ul>
          </b-col>
          <b-col>
            <div class="_hd">Preview</div>
            <ul>
              <li>
                <i class="ion">&#xe7c0;</i> <a href="https://tracesr.github.io/navigation/" target="_blank">移动端导航</a>
              </li>
              <li>
                <i class="ion">&#xe6a5;</i> <a href="https://tracesr.github.io/map-editor/" target="_blank">地图编辑器</a>
              </li>
            </ul>
          </b-col>
          <b-col>
            <div class="_hd">Business</div>
            <ul>
              <li>
                <img src="~assets/img/business.jpg" />
              </li>
            </ul>
          </b-col>
        </b-row>
          
        <p>© Tracesr 2019. All Rights Reserved.</p>
      </b-container>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '觅迹，轻量级室内导航解决方案',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: '觅迹，轻量级室内导航解决方案'
        }
      ]
    }
  },
  data() {
    return {}
  },
  create: function() {}
}
</script>

<style scoped>
.container1 {
  padding-top: 30px;
  margin-bottom:-4rem;
  color:#666;
}

.container1 .subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.container1 .links {
  padding-top: 35px;
}

.container1 .logo {
  height: 200px;
  background: url(~assets/img/logo.png) 0 center no-repeat;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.mockup {
  position: relative;
  width: 320px;
  height: 647px;
  overflow: hidden;
}
.mockup__frame {
  position: absolute;
  display: block;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url(~assets/img/mockup-frame.png);
  background-repeat: no-repeat;
  background-size: contain;
  pointer-events: none;
  z-index: 2;
}
.mock_code {
  position: absolute;
  left: -100%;
  top: 0;
  width: 100%;
  height: 100%;
  background: url(http://refined-x.com/asset/navigation-demo.png) center
    no-repeat;
}
.mockup__video {
  display: block;
  width: 100%;
  height: auto;
  padding: 20% 2.5% 0;
}
.mockup:hover .mock_code {
  left: 0;
}

.container2{background:#26d6b1;padding:10rem 0 2rem;color:#fff;}
.container2 a{color:#06c5bf;}

.container2 .title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: inline-block;
  font-weight: 700;
  font-size: 130px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 30px;
  color: transparent;
    background: url(~assets/img/logob.jpg) no-repeat 0 center;
    background-size: 150% auto;
    background-clip: text;
    animation: bgmove 10s infinite ;
}
@keyframes bgmove
{
    0% {background-position: center top;background-size: 150% auto;}
    10% {background-position: right top;background-size: 150% auto;}
    15% {background-position: right top;background-size: 150% auto;}
    25% {background-position: center top;background-size: 150% auto;}
    30% {background-position: center top;background-size: 150% auto;}
    45% {background-position: center center;background-size: 200% auto;}
    50% {background-position: center center;background-size: 200% auto;}
    75% {background-position: center bottom;background-size: 100% auto;}
    80% {background-position: center bottom;background-size: 100% auto;}
    95% {background-position: center top;background-size: 150% auto;}
    100% {background-position: center top;background-size: 150% auto;}
}
.container2 .subt{font-size:32px;color:#434343;}
.container2 ._tip{margin-top:4rem;text-align: center;font-size:12px;}

.featureList{margin-top: 3rem;}
.featureList li{font-size:16px;padding:6px 0;}
.featureList .ion{margin-right:.5em;}
.featureList ._hd{font-size:26px;margin-bottom: 20px;}

.container3{background:#f8f8f8;padding:6rem 0;color:#000;}
.container3 a{color:#fff;}

.footer {
  padding: 4rem 0;
  color: #fff;
  text-align: center;
  background-image: linear-gradient(to top right, #03928f, #1eab8d);
}
.footer ._main{margin-bottom: 3rem;}
.footer a{color:#fff;}
.footer .ion{color:#333;}
.footer ._links{text-align: left;}
.footer ._hd{font-weight: 700;margin-bottom:2rem;text-align: center}
.footer li{margin-bottom: 10px;}
.footer li img{max-height: 7em;}
</style>
