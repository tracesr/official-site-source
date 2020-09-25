<template>
  <div class="docsPage">
    <b-navbar toggleable="md" type="dark" variant="info" class="my-3">
      <b-navbar-brand href="/">Tracesr - 觅迹导航</b-navbar-brand>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="https://refined-x.com/" target="_blank"
          >Blog</b-nav-item
        >
        <b-nav-item href="https://github.com/tracesr/" target="_blank"
          >Github</b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>

    <b-container>
      <b-breadcrumb :items="items" class="my-3" />
      <h2 class="my-3">介绍</h2>
      <div class="p-3">
        <p>
          觅迹是一套轻量级室内导航解决方案，可以应用于商超、景点、园区等区域寻路场景，结合使用场景可以扩展全局消息、商户消息等多样化营销功能。
          导航系统采用纯前端寻路引擎，反应迅捷，支持主题定制；
        </p>

        <p>
          配套的地图编辑器支持SVG格式图形导入、商户分类、信息编辑、消息发布等功能；
        </p>

        <p>觅迹还自带一套营销页模板，可以为商户实现多样化的营销功能。</p>
      </div>

      <h2 class="my-3">操作手册</h2>

      <h3 class="my-3">导航系统</h3>

      <h4>界面介绍</h4>
      <div class="p-3">
        <p><strong>指北针</strong> 界面左上角，箭头指向北方。</p>
        <p>
          <strong>快捷操作栏</strong>
          界面右上角，包含界面放大/缩小和全局公告按钮。
        </p>
        <p><strong>地图主界面</strong> 界面中部主体部分。</p>
        <p>
          <strong>导航栏</strong>
          界面底部，包含“发现”、“楼层”、“搜索”、“方向锁定”功能。
        </p>
        <p class="my-3">
          <img src="~assets/img/doc1.png" style="max-width: 480px" />
        </p>
      </div>

      <h4>导航功能</h4>
      <div class="p-3">
        <ul>
          <li>
            1.
            点击地图上任意商户，弹出商户面板，操作按钮将商户选择为导航起点或者导航终点
          </li>
          <li>
            2.
            此时将打开导航准备面板，再次在地图上点击商户选择终点或起点，面板底部的“开始导航”按钮将变为可用状态
          </li>
          <li>
            3.
            点击“开始导航”系统将自动寻路，并将导航路径呈现在地图主界面上，同时打开导航结果面板
          </li>
          <li>
            4.
            导航结果面板将分布呈现导航步骤，左右滑动可以切换当前所在步骤，点击“关闭”按钮结束导航
          </li>
        </ul>
        <p class="my-3">
          <img src="~assets/img/doc4.png" style="max-width: 480px" />
        </p>
        <p class="my-3">
          <img src="~assets/img/doc6.png" style="max-width: 480px" />
        </p>
        <p class="my-3">
          <img src="~assets/img/doc7.png" style="max-width: 480px" />
        </p>
        <p class="my-3">
          <img src="~assets/img/doc3.png" style="max-width: 480px" />
        </p>
      </div>

      <h4>公告系统</h4>
      <div class="p-3">
        <p>
          <strong>全局公告</strong>
          通过界面右上角消息按钮打开全局消息面板，展示全局消息，点击消息底部的商户链接可以自动在地图上定位到该商户。
        </p>
        <p>
          <strong>商户公告</strong>
          商户发布的非全局公告将展示在商户面板中，商户公告的曝光效果不如全局公告。
        </p>
        <p class="my-3">
          <img src="~assets/img/doc2.png" style="max-width: 480px" />
        </p>
        <p class="my-3">
          <img src="~assets/img/doc0.jpg" style="max-width: 480px" />
        </p>
      </div>

      <h4>楼层选择</h4>
      <div class="p-3">
        <p>
          选择楼层界面使用3D效果呈现所有楼层，点击楼层标识文字可以进入对应楼层地图。
        </p>
        <p class="my-3">
          <img src="~assets/img/doc5.png" style="max-width: 480px" />
        </p>
      </div>

      <h3 class="my-3">地图编辑器</h3>
      <p class="p-3">正在完善...</p>
    </b-container>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "使用帮助-觅迹",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "觅迹，轻量级室内导航解决方案",
        },
      ],
    };
  },
  data() {
    return {
      items: [
        {
          text: "首页",
          href: "/",
        },
        {
          text: "使用帮助",
          href: "/docs",
        },
      ],
    };
  },
  create: function () {},
};
</script>

<style scoped>
.docsPage .logo {
  height: 100px;
  background: url(~assets/img/logo.png) 0 center no-repeat;
}
</style>
