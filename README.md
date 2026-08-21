# 餐厅开业筹备甘特图

一个交互式的网页甘特图，用于管理餐厅开业全流程的进度跟踪和采购管理。

## 在线访问

部署到 Vercel 后，通过以下链接访问：
```
https://你的项目名.vercel.app
```

## 功能特性

- **甘特图时间轴**：横轴从 8/1 到 10/1，每天一格，周末自动灰底标识
- **今天标记**：蓝色竖线标注当前日期，顶部显示距离开业倒计时
- **五色分类**：证照(蓝)、装修(红)、采购(绿)、人员(紫)、营销(灰)
- **状态自动计算**：根据子任务完成比例自动显示「未开始 / 进行中 / 已完成」
- **子任务管理**：展开/折叠、勾选完成、直接编辑、删除
- **采购清单表格**：名称、数量、预算、付款方式、出货/到货标记
- **localStorage 自动保存**：刷新页面数据不丢失
- **导出HTML**：点击按钮下载包含当前数据的完整文件
- **深色模式**：自动跟随系统主题切换

## 部署到 Vercel

### 方式一：通过 GitHub 自动部署（推荐）

1. 将本项目推送到 GitHub 仓库
2. 登录 [vercel.com](https://vercel.com)（用 GitHub 账号）
3. 点击 **Add New Project**
4. 导入你的 GitHub 仓库
5. Framework Preset 选 **Other**
6. 点击 **Deploy**

之后每次 push 代码到 GitHub，Vercel 会自动重新部署。

### 方式二：直接上传

1. 登录 [vercel.com](https://vercel.com)
2. 点击 **Add New Project**
3. 选择 **Import Git Repository** 下方的 **Upload** 选项
4. 将整个项目文件夹压缩为 zip 上传
5. 点击 **Deploy**

## 数据同步说明

由于这是纯静态网页，修改保存在浏览器 localStorage 中：

```
在网页上修改 → 自动保存到浏览器
→ 改完后点击「导出HTML」
→ 下载新文件 → 替换仓库里的 index.html
→ git push → Vercel 自动更新
```

## 文件结构

```
opening-gantt/
├── index.html      # 主页面（包含所有代码）
├── vercel.json     # Vercel 部署配置
└── README.md       # 项目说明
```

## 技术栈

- 纯 HTML + CSS + JavaScript（零依赖）
- 支持现代浏览器
- 响应式设计
- 支持 prefers-color-scheme 深色模式

## 作者

由 Kimi AI 辅助生成，可根据实际业务需求自由修改。
