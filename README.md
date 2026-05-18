# NearGo 餐饮 OMS — 交互演示

> **设计规范验证项目** · 基于 [NearGo OMS Design System v3.2](https://github.com/zoezou7788/neargo-oms-design-system) 构建

**🔗 在线预览：** https://zoezou7788.github.io/neargo-restaurant-oms-demo

---

## 功能模块

| 页面 | 功能 |
|------|------|
| 📊 系统概览 | KPI 指标卡、销售折线图、菜品销量排行、最新订单、动态流 |
| 🛒 订单管理 | 数据表格、状态筛选、搜索、接单操作、订单详情弹窗 |
| 🏪 门店管理 | 门店列表、新增门店表单（含校验）、状态管理 |
| 🍽️ 菜品管理 | 卡片/表格双视图切换、Tabs 分类筛选、新增菜品 |
| 👥 员工管理 | 员工列表、角色徽章、离职操作 |
| 🎁 优惠活动 | 活动卡片展示、品牌色克制使用验证 |
| 📈 数据报表 | 门店排行横向条形图、订单类型环形图 |

## 验证的设计规范点

- ✅ `#1F1D1C` 主色驱动所有关键操作按钮
- ✅ `#FFA902` 品牌色仅用于「热销」Badge 和「创建活动」按钮（≤10%）
- ✅ Radix 12步色阶语义色：成功/危险/信息/警告/紫色全部对应正确
- ✅ 所有状态指示器采用「色点 + 文字」双通道（无障碍合规）
- ✅ 深色模式一键切换（topbar 右上角🌙）
- ✅ `--shadow-2` 卡片阴影，`--radius-4` 标准圆角，`--radius-5` Dialog 圆角
- ✅ Motion tokens：Dialog fade-in、Toast slide-in-right、卡片 hover 抬升
- ✅ z-index 层叠：Toast(600) > Modal(400) > Overlay(300) > Sticky(200)
- ✅ 表单校验：必填、手机号格式、错误高亮 + Toast 提示
- ✅ `prefers-reduced-motion` 媒体查询响应

## 技术栈

纯 HTML + CSS + 原生 JS（无依赖，GitHub Pages 直接部署）

所有样式变量直接引用设计规范中的 CSS Token，无硬编码 Hex 值。
