# 基础数据管理 - 菜单配置文档

本文档提供"基础数据管理"模块的完整菜单结构配置信息。

## ✅ 当前状态：已启用临时静态路由

**✨ 好消息！为了方便开发，我们已经添加了临时的静态路由配置。**

现在您可以：

1. ✅ **立即在左侧菜单栏看到"基础数据管理"模块**
2. ✅ **直接访问所有 24 个子页面进行开发**
3. ✅ **无需等待后端配置即可进行界面开发**

### 📁 静态路由配置文件

- `src/router/modules/baseData.ts` - 基础数据管理模块静态路由
- `src/router/modules/remaining.ts` - 已引入基础数据管理路由

### ⚠️ 后续迁移说明

当您准备对接后端时，只需：

1. 在后端系统中按照本文档配置菜单
2. 删除或注释掉 `src/router/modules/baseData.ts` 文件
3. 删除 `src/router/modules/remaining.ts` 中对 `baseDataRouter` 的引入和使用

---

## 🔄 后端动态菜单配置（可选 - 后期对接时使用）

本项目的菜单系统支持**后端动态加载**，这是正式环境推荐的方式。以下是后端配置步骤：

### 快速配置步骤

1. **登录后端管理系统**
2. **进入：系统管理 → 菜单管理**
3. **按照下面的层级结构依次创建菜单**
4. **刷新前端页面，菜单即可显示**

📄 **详细的菜单配置 JSON 数据请查看：`BASEDATA_MENU_IMPORT.json`**

## 📋 菜单层级总览

```
基础数据管理 (base-data)
├── 安防设备相关 (security-device)
│   ├── 监控设备 (monitor-device)
│   ├── 边缘网关管理 (edge-gateway)
│   ├── 分析任务 (analysis-task)
│   ├── 智能订阅 (smart-subscription)
│   └── 明厨亮灶 (bright-kitchen)
├── 物联设备感知 (iot-sensor)
│   ├── 温湿度传感器 (temperature-humidity)
│   ├── 周界报警主机 (perimeter-alarm)
│   └── 物联设备 (iot-device)
├── 门禁设备管理 (access-control)
│   ├── 门禁设备 (access-device)
│   ├── 门禁时间段 (time-period)
│   └── 门禁权限组 (permission-group)
├── 道闸设备管理 (barrier-gate)
│   ├── 道闸设备 (barrier-device)
│   └── 车场管理 (parking-lot)
├── 系统资源管理 (system-resource)
│   ├── 分组管理 (group)
│   ├── 场景地图 (scene-map)
│   ├── 联动管理 (linkage)
│   ├── 事件配置 (event-config)
│   └── 媒体服务 (media-service)
├── 巡更设备配置 (patrol)
│   ├── 巡检器管理 (patrol-device)
│   ├── 巡检点管理 (patrol-point)
│   └── 线路管理 (patrol-route)
└── 建筑区域配置 (building-area)
```

## 🎯 路由路径映射表

| 菜单名称 | 路由路径 | 组件名称 | 图标建议 |
| --- | --- | --- | --- |
| **基础数据管理** | `/base-data` | Layout | `ep:setting` |
| 监控设备 | `/base-data/security-device/monitor-device` | `BaseDataMonitorDevice` | `ep:video-camera` |
| 边缘网关管理 | `/base-data/security-device/edge-gateway` | `BaseDataEdgeGateway` | `ep:connection` |
| 分析任务 | `/base-data/security-device/analysis-task` | `BaseDataAnalysisTask` | `ep:data-analysis` |
| 智能订阅 | `/base-data/security-device/smart-subscription` | `BaseDataSmartSubscription` | `ep:bell` |
| 明厨亮灶 | `/base-data/security-device/bright-kitchen` | `BaseDataBrightKitchen` | `ep:food` |
| 温湿度传感器 | `/base-data/iot-sensor/temperature-humidity` | `BaseDataTemperatureHumidity` | `ep:partly-cloudy` |
| 周界报警主机 | `/base-data/iot-sensor/perimeter-alarm` | `BaseDataPerimeterAlarm` | `ep:warning` |
| 物联设备 | `/base-data/iot-sensor/iot-device` | `BaseDataIoTDevice` | `ep:platform` |
| 门禁设备 | `/base-data/access-control/access-device` | `BaseDataAccessControlDevice` | `ep:lock` |
| 门禁时间段 | `/base-data/access-control/time-period` | `BaseDataAccessControlTimePeriod` | `ep:clock` |
| 门禁权限组 | `/base-data/access-control/permission-group` | `BaseDataAccessControlPermissionGroup` | `ep:user` |
| 道闸设备 | `/base-data/barrier-gate/barrier-device` | `BaseDataBarrierGateDevice` | `ep:guide` |
| 车场管理 | `/base-data/barrier-gate/parking-lot` | `BaseDataParkingLot` | `ep:parking` |
| 分组管理 | `/base-data/system-resource/group` | `BaseDataSystemGroup` | `ep:folder` |
| 场景地图 | `/base-data/system-resource/scene-map` | `BaseDataSceneMap` | `ep:map-location` |
| 联动管理 | `/base-data/system-resource/linkage` | `BaseDataLinkage` | `ep:link` |
| 事件配置 | `/base-data/system-resource/event-config` | `BaseDataEventConfig` | `ep:setting` |
| 媒体服务 | `/base-data/system-resource/media-service` | `BaseDataMediaService` | `ep:video-play` |
| 巡检器管理 | `/base-data/patrol/patrol-device` | `BaseDataPatrolDevice` | `ep:compass` |
| 巡检点管理 | `/base-data/patrol/patrol-point` | `BaseDataPatrolPoint` | `ep:location` |
| 线路管理 | `/base-data/patrol/patrol-route` | `BaseDataPatrolRoute` | `ep:route` |
| 建筑区域配置 | `/base-data/building-area` | `BaseDataBuildingArea` | `ep:office-building` |

## 💾 后端菜单配置SQL示例（参考）

```sql
-- 一级菜单：基础数据管理
INSERT INTO system_menu (name, permission, type, sort, parent_id, path, icon, component, status)
VALUES ('基础数据管理', '', 1, 100, 0, '/base-data', 'ep:setting', 'Layout', 0);

-- 二级菜单：安防设备相关
INSERT INTO system_menu (name, permission, type, sort, parent_id, path, icon, component, status)
VALUES ('安防设备相关', '', 1, 1, @base_data_id, 'security-device', 'ep:video-camera', '', 0);

-- 三级菜单：监控设备
INSERT INTO system_menu (name, permission, type, sort, parent_id, path, icon, component, status)
VALUES ('监控设备', 'base-data:monitor-device:query', 2, 1, @security_device_id, 'monitor-device', 'ep:video-camera', 'base-data/security-device/monitor-device/index', 0);

-- ... 依次类推
```

## 🔑 权限标识符建议

| 功能模块 | 查询权限 | 新增权限 | 修改权限 | 删除权限 |
| --- | --- | --- | --- | --- |
| 监控设备 | `base-data:monitor-device:query` | `base-data:monitor-device:create` | `base-data:monitor-device:update` | `base-data:monitor-device:delete` |
| 边缘网关 | `base-data:edge-gateway:query` | `base-data:edge-gateway:create` | `base-data:edge-gateway:update` | `base-data:edge-gateway:delete` |
| ... | ... | ... | ... | ... |

## ⚠️ 重要说明

为避免组件命名冲突，已对以下路径进行了调整：

- 门禁设备：`device` → `access-device`
- 道闸设备：`device` → `barrier-device`

这样可以避免 Vue 组件自动导入插件的命名冲突问题。

## 📁 已创建的文件清单

### Views 层（占位页面）

- ✅ `src/views/base-data/security-device/monitor-device/index.vue`
- ✅ `src/views/base-data/security-device/edge-gateway/index.vue`
- ✅ `src/views/base-data/security-device/analysis-task/index.vue`
- ✅ `src/views/base-data/security-device/smart-subscription/index.vue`
- ✅ `src/views/base-data/security-device/bright-kitchen/index.vue`
- ✅ `src/views/base-data/iot-sensor/temperature-humidity/index.vue`
- ✅ `src/views/base-data/iot-sensor/perimeter-alarm/index.vue`
- ✅ `src/views/base-data/iot-sensor/iot-device/index.vue`
- ✅ `src/views/base-data/access-control/access-device/index.vue`
- ✅ `src/views/base-data/access-control/time-period/index.vue`
- ✅ `src/views/base-data/access-control/permission-group/index.vue`
- ✅ `src/views/base-data/barrier-gate/barrier-device/index.vue`
- ✅ `src/views/base-data/barrier-gate/parking-lot/index.vue`
- ✅ `src/views/base-data/system-resource/group/index.vue`
- ✅ `src/views/base-data/system-resource/scene-map/index.vue`
- ✅ `src/views/base-data/system-resource/linkage/index.vue`
- ✅ `src/views/base-data/system-resource/event-config/index.vue`
- ✅ `src/views/base-data/system-resource/media-service/index.vue`
- ✅ `src/views/base-data/patrol/patrol-device/index.vue`
- ✅ `src/views/base-data/patrol/patrol-point/index.vue`
- ✅ `src/views/base-data/patrol/patrol-route/index.vue`
- ✅ `src/views/base-data/building-area/index.vue`

**共计：24 个页面文件**

## 📝 后端菜单配置详细步骤

### 第一步：添加一级菜单 - 基础数据管理

进入 `系统管理` → `菜单管理`，点击"新增"按钮：

| 配置项       | 值           | 说明              |
| ------------ | ------------ | ----------------- |
| **上级菜单** | 主类目       | 选择顶级菜单      |
| **菜单名称** | 基础数据管理 |                   |
| **菜单类型** | 目录         |                   |
| **路由地址** | `base-data`  | 不要加前缀 `/`    |
| **菜单图标** | `ep:setting` | Element Plus 图标 |
| **组件路径** | `Layout`     | 必须填 Layout     |
| **显示排序** | 100          | 根据实际需求调整  |
| **显示状态** | 显示         | ✅                |
| **菜单状态** | 正常         | ✅                |

### 第二步：添加二级菜单（目录）

以"安防设备相关"为例：

| 配置项       | 值                |
| ------------ | ----------------- |
| **上级菜单** | 基础数据管理      |
| **菜单名称** | 安防设备相关      |
| **菜单类型** | 目录              |
| **路由地址** | `security-device` |
| **菜单图标** | `ep:video-camera` |
| **显示排序** | 1                 |

按此方式添加其他二级目录：

- 物联设备感知（`iot-sensor`）
- 门禁设备管理（`access-control`）
- 道闸设备管理（`barrier-gate`）
- 系统资源管理（`system-resource`）
- 巡更设备配置（`patrol`）

### 第三步：添加三级菜单（实际页面）

以"监控设备"为例：

| 配置项       | 值                                               | 说明                   |
| ------------ | ------------------------------------------------ | ---------------------- |
| **上级菜单** | 安防设备相关                                     |                        |
| **菜单名称** | 监控设备                                         |                        |
| **菜单类型** | 菜单                                             | 注意是"菜单"不是"目录" |
| **路由地址** | `monitor-device`                                 |                        |
| **菜单图标** | `ep:video-camera`                                |                        |
| **组件路径** | `base-data/security-device/monitor-device/index` | 相对于 `src/views/`    |
| **组件名称** | `BaseDataMonitorDevice`                          | 用于路由缓存           |
| **权限标识** | `base-data:monitor-device:query`                 | 格式：模块:功能:操作   |
| **显示排序** | 1                                                |                        |
| **是否缓存** | ✅ 缓存                                          |                        |
| **显示状态** | ✅ 显示                                          |                        |
| **菜单状态** | ✅ 正常                                          |                        |

### 第四步：为角色分配权限

1. 进入 `系统管理` → `角色管理`
2. 编辑管理员角色（或您当前使用的角色）
3. 在菜单权限中勾选"基础数据管理"及其子菜单
4. 保存后**退出登录，重新登录**

### 第五步：验证

刷新页面，您应该能在左侧菜单栏看到"基础数据管理"模块及其所有子菜单。

---

## 🎯 配置要点

### 关键字段说明

| 字段 | 说明 | 示例 |
| --- | --- | --- |
| **type** | 0=按钮, 1=目录, 2=菜单 | 一级用1，二级目录用1，三级页面用2 |
| **component** | 一级必须是 `Layout`<br>二级目录为空<br>三级填页面路径 | `base-data/security-device/monitor-device/index` |
| **componentName** | 用于 keep-alive 缓存 | 驼峰命名：`BaseDataMonitorDevice` |
| **path** | 路由地址，不要加 `/` 前缀 | `monitor-device` |
| **permission** | 权限标识 | `base-data:monitor-device:query` |

### 常见错误

❌ **组件路径错误**

- 错误：`/base-data/...` 或 `src/views/base-data/...`
- 正确：`base-data/security-device/monitor-device/index`

❌ **路由地址错误**

- 错误：`/monitor-device`
- 正确：`monitor-device`

❌ **一级菜单组件错误**

- 错误：留空或填其他
- 正确：必须填 `Layout`

---

## 📦 完整配置参考

详细的 JSON 格式配置数据请查看：**`BASEDATA_MENU_IMPORT.json`**

该文件包含：

- ✅ 完整的 24 个菜单项配置
- ✅ 所有必填字段和可选字段
- ✅ 详细的字段说明和注释
- ✅ 配置规范和最佳实践

---

## 🚀 后续操作

1. ✅ **配置菜单**（按上述步骤操作）
2. ✅ **分配权限**（为角色勾选菜单权限）
3. ✅ **重新登录**（使权限生效）
4. 🎯 **开始具体功能开发**
   - 选择优先级最高的模块开始开发
   - 建议从"建筑区域配置"或"监控设备"开始
   - 参考现有的"设备档案"或"实时预览"功能进行开发

## 🎨 占位页面特性

所有占位页面均包含：

- ✅ 明暗模式适配
- ✅ 模块归属说明
- ✅ 功能描述
- ✅ 统一的 UI 风格
- ✅ 响应式布局

---

**菜单架构已建立完成，可以开始具体功能开发！** 🚀
