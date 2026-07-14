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

      <nav class="docs-toc p-3 mb-3">
        <p class="mb-2"><strong>目录</strong></p>
        <ul class="mb-0">
          <li><a href="#intro">介绍</a></li>
          <li>
            <a href="#manual">操作手册</a>
            <ul>
              <li><a href="#nav-manual">导航系统</a></li>
              <li><a href="#editor-manual">地图编辑器</a></li>
            </ul>
          </li>
          <li>
            <a href="#tech">技术文档</a>
            <ul>
              <li><a href="#tech-arch">系统架构</a></li>
              <li><a href="#tech-nav">导航前端</a></li>
              <li><a href="#tech-editor">地图编辑器数据流水线</a></li>
              <li><a href="#tech-format">数据格式约定</a></li>
              <li><a href="#tech-publish">从编辑到上线</a></li>
            </ul>
          </li>
        </ul>
      </nav>

      <h2 id="intro" class="my-3">介绍</h2>
      <div class="p-3">
        <p>
          觅迹是一套轻量级室内导航解决方案，可以应用于商超、景点、园区等区域寻路场景，结合使用场景可以扩展全局消息、商户消息等多样化营销功能。
          导航系统采用纯前端寻路引擎，反应迅捷，支持主题定制；
        </p>

        <p>
          配套的地图编辑器支持 SVG 格式图形导入、商户分类、信息编辑、路径图绘制与
          JSON 数据导出等功能；
        </p>

        <p>觅迹还自带一套营销页模板，可以为商户实现多样化的营销功能。</p>
      </div>

      <h2 id="manual" class="my-3">操作手册</h2>

      <h3 id="nav-manual" class="my-3">导航系统</h3>

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

      <h4>搜索与方向锁定</h4>
      <div class="p-3">
        <p>
          <strong>搜索</strong>
          点击底栏「搜索」进入关键词搜索页，系统按商铺标题（优先）与描述进行模糊匹配。选中结果后返回地图并自动打开对应商户面板，可继续设为起点或终点。
        </p>
        <p>
          <strong>方向锁定</strong>
          底栏「旋转」用于切换地图方向模式：锁定时地图朝向固定；解锁后可跟随设备朝向旋转，并与左上角指北针联动。部分浏览器需授权设备方向权限后才能生效。
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

      <h3 id="editor-manual" class="my-3">地图编辑器</h3>

      <h4>界面与双模式</h4>
      <div class="p-3">
        <p>
          地图编辑器是离线桌面式工具，在固定
          <strong>1000×1000</strong> 像素画布上编辑室内平面图与道路网，导出
          <code>map.json</code> / <code>path.json</code> 供导航前端使用。编辑器本身<strong>没有服务端</strong>，数据保存在浏览器会话或本地导出文件中。
        </p>
        <p>主界面提供两种工作模式：</p>
        <ul>
          <li>
            <strong>编辑地图</strong>：选中商铺/区域多边形，编辑标题、描述、业态类型、关联路径节点及是否忽略建筑。
          </li>
          <li>
            <strong>路径绘制</strong>：在画布上绘制可行走道路径节点，管理多条路径、命名、拖拽与表格编辑坐标。
          </li>
        </ul>
        <p class="my-3">
          <img src="~assets/img/editer.png" style="max-width: 480px" />
        </p>
        <p class="my-3">
          <img src="~assets/img/doc8.png" style="max-width: 480px" />
        </p>
      </div>

      <h4>导入数据</h4>
      <div class="p-3">
        <p>通过导入面板可加载四类本地文件：</p>
        <ul>
          <li>
            <strong>置入底图</strong>（<code>*.png</code>）：作为画布背景参考图。
          </li>
          <li>
            <strong>导入地图文件</strong>（<code>map.svg</code>）：解析
            <code>polygon</code> / <code>rect</code>，读取标题与中心点；缺失时自动计算多边形中心。
          </li>
          <li>
            <strong>导入地图数据</strong>（<code>map.json</code>）：加载已编辑的商铺多边形数组。
          </li>
          <li>
            <strong>导入路径数据</strong>（<code>path.json</code>）：支持
            schemaVersion 2 格式，以及旧版纯数组格式（自动补全路径名称）。
          </li>
        </ul>
        <p>
          也可点击「体验数据」从站点静态资源加载演示用的
          <code>map.json</code> / <code>path.json</code>。
        </p>
      </div>

      <h4>编辑地图</h4>
      <div class="p-3">
        <p>在「编辑地图」模式下选中多边形后，可配置：</p>
        <ul>
          <li><strong>标题</strong>（<code>attrTitle</code>）：商铺名称，导航搜索与寻路锚点。</li>
          <li><strong>描述</strong>（<code>desc</code>）：可选说明，参与搜索匹配。</li>
          <li>
            <strong>所属类型</strong>（<code>type</code>）：业态配色，内置餐饮、服装、百货、娱乐、美容美发、电子数码六类。
          </li>
          <li>
            <strong>关联路径节点</strong>（<code>connectPoint</code>）：商铺在道路图上的入口坐标，寻路起终点必须指向有效节点。
          </li>
          <li>
            <strong>忽略建筑物</strong>（<code>block</code>）：标记为非商铺区域（如墙体），导航端不参与搜索列表。
          </li>
        </ul>
      </div>

      <h4>路径绘制</h4>
      <div class="p-3">
        <ul>
          <li>支持多条路径：每条路径有名称（<code>names</code>）与有序节点数组（<code>roads</code>）。</li>
          <li>节点可点击绘制、拖拽移动，或在表格中手输坐标；支持前/后插入、删除节点。</li>
          <li>
            <strong>共享节点</strong>（<code>connect: true</code>）：多路径交汇点，拖拽时会同步更新所有路径上的同坐标点。
          </li>
          <li>
            节点可绑定 <code>connectBuildings</code>，与商铺的
            <code>connectPoint</code> 双向关联，保证导航起终点落在路网图上。
          </li>
        </ul>
      </div>

      <h4>导出与校验</h4>
      <div class="p-3">
        <p>
          工具栏可分别下载 <code>map.json</code> 与
          <code>path.json</code>。导出路径前会自动编译加权图
          <code>graph</code> 并做质量检查：
        </p>
        <ul>
          <li>
            <strong>错误（阻止导出）</strong>：如道路数据无效、节点坐标非法、零长度边、商铺关联节点不存在等。
          </li>
          <li>
            <strong>警告（允许导出）</strong>：如重复边、孤立节点、图不连通、路径相交但未设连接节点等。
          </li>
        </ul>
        <p>
          编辑过程中，当前多边形与路径会写入
          <code>sessionStorage</code>，刷新页面后可「恢复数据」；也可「清空数据」重置画布。
        </p>
      </div>

      <h2 id="tech" class="my-3">技术文档</h2>

      <h3 id="tech-arch" class="my-3">系统架构</h3>
      <div class="p-3">
        <p>觅迹由三个主要仓库组成：</p>
        <ul>
          <li>
            <strong>map-editor-source-2</strong>：地图/路径生产工具（纯前端），产出
            <code>map.json</code> 与 <code>path.json</code>。
          </li>
          <li>
            <strong>navigation-source-2</strong>：移动端导航演示应用，静态打包楼层数据并消费预编译
            <code>graph</code> 做最短路径寻路。
          </li>
          <li>
            <strong>official-site-source</strong>：官网与本文档源码，构建后发布到
            <code>tracesr.github.io</code>。
          </li>
        </ul>
        <p>典型数据流：</p>
        <ol>
          <li>在地图编辑器中编辑并导出 <code>map.json</code> / <code>path.json</code></li>
          <li>（可选）执行 <code>npm run generate:path</code> 补全/校验 <code>graph</code></li>
          <li>
            将文件拷贝到
            <code>navigation-source-2/src/assets/maps/{floor}/</code>，并准备
            <code>layout.png</code>、<code>preview.png</code>
          </li>
          <li>在 <code>maps/index.js</code> 注册楼层</li>
          <li>导航端构建后，由 <code>pathfinding.js</code> 基于 Dijkstra 消费 <code>graph</code></li>
        </ol>
        <p>
          <strong>说明：</strong>地图数据走前端静态打包，不经过在线 CRUD API。导航端可选接入远程公告接口；地图编辑器无鉴权、无服务端存储、无一键云端发布。
        </p>
      </div>

      <h3 id="tech-nav" class="my-3">导航前端</h3>
      <div class="p-3">
        <h5>技术栈</h5>
        <p>
          Vue 2.7 + Vue Router 3 + Vite 3，UI 使用 cube-ui（移动端），兼容构建目标含 IE11（legacy
          插件）。
        </p>

        <h5>路由与页面</h5>
        <ul>
          <li><code>/</code> → 重定向到 <code>/map/1F</code></li>
          <li><code>/map/:name</code>：楼层地图与导航主界面</li>
          <li><code>/maps</code>：3D 楼层选择器</li>
          <li><code>/search</code>：商铺关键词搜索</li>
        </ul>

        <h5>寻路链路</h5>
        <ol>
          <li>用户选定起终点商铺，读取各自的 <code>connectPoint</code></li>
          <li>
            <code>core.startSearch</code> 调用
            <code>pathfinding.js</code>，在无向加权图上跑 Dijkstra
          </li>
          <li>
            <code>core.navigate</code> 将折线路径整理为逐步指引文案（方向 + 距离，单位米）
          </li>
          <li>主界面用 SVG <code>polyline</code> 绘制路径，并用轮播展示步骤</li>
        </ol>

        <h5>渲染层</h5>
        <p>
          画布固定 1000×1000：底图（<code>layout.png</code>）+ SVG 商铺多边形层 + 路径层 +
          漂浮标题层（标题随地图旋转做反向补偿）。
        </p>

        <h5>已支持特性</h5>
        <ul>
          <li>商铺点击高亮、分类着色、起终点导航、路径可视化与逐步文字指引</li>
          <li>关键词搜索（标题 / 描述）、楼层选择 UI、地图 5 档缩放</li>
          <li>指北针与设备方向跟随、全局/商户公告（远程 API）</li>
        </ul>

        <h5>当前限制</h5>
        <ul>
          <li>演示数据默认仅注册 <strong>1F</strong>；无跨楼层路径</li>
          <li>无蓝牙 / UWB / GPS 室内实时定位，起终点需手动选择</li>
          <li>底栏「发现」为占位功能</li>
          <li>商铺若缺少有效 <code>connectPoint</code>，无法参与寻路</li>
        </ul>
      </div>

      <h3 id="tech-editor" class="my-3">地图编辑器数据流水线</h3>
      <div class="p-3">
        <h5>定位</h5>
        <p>
          纯前端 SPA。「发布」含义是：在浏览器中导出 JSON，再手工集成到导航工程并重新构建——不是调用服务端发布接口。
        </p>

        <h5>导入 / 导出</h5>
        <ul>
          <li>导入：浏览器 <code>FileReader</code> 读取本地 PNG / SVG / JSON</li>
          <li>导出：生成 Blob URL 触发 <code>&lt;a download&gt;</code> 下载</li>
          <li>
            会话：<code>sessionStorage</code> 键
            <code>editing-polygons</code>、<code>editing-roads</code> 保存编辑现场
          </li>
        </ul>

        <h5>图编译</h5>
        <p>
          核心逻辑在 <code>src/assets/graph.js</code>：由
          <code>roads</code> 生成无向加权图
          <code>graph</code>（节点 ID 为 <code>"x,y"</code>，边权 =
          像素欧氏距离 × <code>metersPerPixel</code>）。
        </p>
        <p>
          构建期也可使用 CLI（无需打开编辑器 UI）：
        </p>
        <pre class="docs-pre">npm run generate:path
# 等价于:
# node scripts/generate-path-data.mjs public/path.json public/map.json --pretty</pre>

        <h5>坐标系</h5>
        <ul>
          <li>画布：1000×1000 px，原点左上，X 向右，Y 向下</li>
          <li>默认 <code>metersPerPixel = 0.1</code>（与导航端距离比例一致）</li>
          <li><code>graph.directed</code> 必须为 <code>false</code>，<code>weightUnit</code> 为 <code>"meter"</code></li>
        </ul>
      </div>

      <h3 id="tech-format" class="my-3">数据格式约定</h3>
      <div class="p-3">
        <h5>map.json</h5>
        <p>类型为多边形记录数组。单条示意：</p>
        <pre class="docs-pre">{
  "points": "104.333,293.667 118,241 ...",
  "attrDataX": 149,
  "attrDataY": 278,
  "attrTitle": "美特斯邦威",
  "type": { "title": "服装", "fill": "#fece8b", "stroke": "#e0b170" },
  "desc": "可选描述",
  "block": false,
  "connectPoint": {
    "x": 203,
    "y": 315,
    "connectBuildings": ["美特斯邦威"]
  }
}</pre>
        <ul>
          <li><code>points</code>：SVG polygon points 字符串</li>
          <li><code>attrDataX</code> / <code>attrDataY</code>：漂浮标题位置</li>
          <li><code>connectPoint</code>：路网入口节点，寻路必需</li>
          <li><code>block: true</code>：非商铺区域</li>
        </ul>

        <h5>path.json（schemaVersion: 2）</h5>
        <pre class="docs-pre">{
  "schemaVersion": 2,
  "scale": { "metersPerPixel": 0.1 },
  "names": ["路径1", "路径2"],
  "roads": [
    [
      { "x": 234, "y": 299, "connect": true },
      { "x": 203, "y": 315, "connectBuildings": ["美特斯邦威"], "connect": true }
    ]
  ],
  "graph": {
    "directed": false,
    "weightUnit": "meter",
    "nodes": [{ "id": "234,299", "x": 234, "y": 299 }],
    "edges": [{ "id": "...", "from": "...", "to": "...", "weight": 3.48 }]
  }
}</pre>
        <p>
          导航端实际使用 <code>path.graph</code>；<code>roads</code> /
          <code>names</code> 主要服务编辑器二次编辑。旧格式若为
          <code>Array&lt;Array&lt;Point&gt;&gt;</code>，导入时会自动升级。
        </p>
      </div>

      <h3 id="tech-publish" class="my-3">从编辑到上线</h3>
      <div class="p-3">
        <ol>
          <li>在地图编辑器完成商铺与路径编辑，导出 <code>map.json</code> 与 <code>path.json</code>。</li>
          <li>
            （推荐）在编辑器工程执行
            <code>npm run generate:path</code>，确认图校验通过并写入完整
            <code>graph</code>。
          </li>
          <li>
            将两份 JSON 放入导航工程
            <code>src/assets/maps/{n}/</code>，并放置该层
            <code>layout.png</code>（底图）、<code>preview.png</code>（楼层预览）。
          </li>
          <li>
            在 <code>src/assets/maps/index.js</code> 注册：
            <pre class="docs-pre">{
  map,
  path,
  name: "1F",
  preview,
  layout
}</pre>
          </li>
          <li>构建并部署导航前端（例如发布到站点的 <code>/navigation/</code> 路径）。</li>
          <li>
            官网文档与营销页：在 <code>official-site-source</code> 执行
            <code>npm run generate</code>，将 <code>dist/</code> 同步到
            <code>tracesr.github.io</code> 后推送。
          </li>
        </ol>
      </div>
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

.docs-toc {
  background: #f7f9fa;
  border: 1px solid #e3e8eb;
  border-radius: 4px;
}

.docs-toc ul {
  padding-left: 1.25rem;
}

.docs-toc a {
  color: #2c7a7b;
}

.docs-pre {
  display: block;
  padding: 0.75rem 1rem;
  margin: 0.75rem 0;
  overflow-x: auto;
  font-size: 0.875rem;
  line-height: 1.45;
  background: #f4f6f8;
  border: 1px solid #e3e8eb;
  border-radius: 4px;
  white-space: pre-wrap;
  word-break: break-word;
}

.docsPage h2[id],
.docsPage h3[id] {
  scroll-margin-top: 1rem;
}
</style>
