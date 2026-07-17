# 录匣 Recxia 模拟面试录制管理系统 — 演示文档

[English](demo.md)

![录匣 Logo](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/logo_256.png)

## 一、产品概述

录匣(RecXia)是一款面向高考面试培训机构的模拟面试录制管理系统，实现"排序→模拟→录制→AI分析→反馈→改进"的完整教学闭环。

### 核心价值

| 价值点 | 说明 |
|--------|------|
| 完整闭环 | 覆盖从报名到家长反馈的全流程 |
| AI 赋能 | 自动语音转文本与智能评测 |
| 多平台 | Web、桌面端、Android、小程序全覆盖 |
| 高效管理 | Excel 批量导入，一键分发 |

### 适用角色

| 角色 | 核心功能 | 访问方式 |
|------|----------|----------|
| 管理员 | 系统维护、用户管理 | Web 浏览器 |
| 教务 | 报名管理、班级分配、缴费状态 | Web 浏览器 |
| 教师 | 创建场次、录制管理、批注、分发 | 桌面应用 / Android App / Web |
| 学员 | 被录制，无需直接操作系统 | — |
| 家长 | 观看视频、查看批注、下载视频 | 微信小程序 / 钉钉小程序 / H5 |

---

## 二、业务流程概述

```
家长报名/教务代报名 → 教务确认缴费 → 分配班级 → 分配教师
    ↓
教师创建模拟场次 → 调整学员顺序 → 开始录制（PC/Android）
    ↓
视频自动上传 → AI 分析生成批注 → 教师审核批注
    ↓
教师分发视频 → 家长收到通知 → 查看视频、批注、下载
```

| 阶段 | 负责人 | 关键动作 |
|------|--------|----------|
| 报名缴费 | 教务 | 学员录入、分班、标记缴费 |
| 创建场次 | 教师 | 选择班级、调整顺序、启动录制 |
| 录制上传 | 教师 | PC 或 Android 录制、自动上传 |
| AI 分析 | 系统 | 语音转文本、生成评价 |
| 审核分发 | 教师 | 查看批注、一键分发 |
| 查看反馈 | 家长 | 小程序查看视频和批注 |

---

## 三、角色详情

### 3.1 家长端

#### 家长注册

家长可通过微信小程序自助注册，填写家长姓名、学生姓名、联系方式等信息：

![小程序家长注册输入](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长注册输入.jpg)

注册成功后系统提示：

![小程序家长注册成功](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长注册成功.jpg)

家长也可通过 WebApp 登录查看：

![WebApp 家长登录](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-登录.png)

#### 家长查看视频

家长通过收到的链接进入视频查看页面：

![WebApp-家长入口](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-家长入口.png)

查看自己孩子的所有模拟面试视频：

![WebApp-学生视频列表](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-学生视频列表.png)

在线播放视频，查看 AI 生成的语音转录文本：

![WebApp-视频预览和语音转录文本](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-视频预览和语音转录文本.png)

![小程序-语音转录](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-语音转录.jpg)

视频播放页面展示教师点评和 AI 分析建议：

![WebApp-教师和AI批注](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-教师和AI批注.png)

![小程序-教师批注](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-教师批注.jpg)

家长点击批注中的时间点，视频会自动跳转到对应位置。

小程序端完整体验：

![小程序-登录](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-登录.jpg)

![小程序-查看录制视频](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频.jpg)

![小程序-看视频](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-看视频.jpg)

### 3.2 教师端

#### 启动录制应用

教师在 Web 端点击「启动录制」按钮，唤起原生录制应用：

![模拟练习-启动模拟练习app](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-启动模拟练习app.png)

#### 创建模拟练习场次

启动录制应用后，教师创建模拟面试场次，选择班级并调整学员顺序：

![模拟练习-创建模拟练习](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-创建模拟练习.png)

创建成功提示：

![模拟练习-创建模拟练习成功](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-创建模拟练习成功.png)

#### Android 端录制流程

教师使用 Android 手机进行课堂录制，灵活便捷：

**步骤1：创建练习场次**

![Android-创建练习场次](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-创建练习场次.jpg)

**步骤2：查看场次列表**

![Android-场次列表](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-场次列表.jpg)

**步骤3：开始录制**

![Android-录制](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制.jpg)

**步骤4：录制中**

![Android-录制中](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制中.jpg)

**步骤5：录制上传**

![Android-录制上传](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制上传.jpg)

**步骤6：上传视频**

![Android-上传](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-上传.jpg)

**步骤7：上传成功**

![Android-上传成功](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-上传成功.jpg)

#### 桌面端录制界面

桌面端提供高质量录制体验，界面清晰显示当前学员、进度和录制状态：

![模拟练习-录制界面](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制界面.png)

![模拟练习-录制中](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制中.png)

![模拟练习-录制完上传](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制完上传.png)

完整的模拟面试录制系统：

![模拟面试录制系统](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟面试录制系统.png)

#### 视频管理与批注

教师在 Web 端查看所有录制的视频，支持按场次、学员筛选：

![视频管理-总界面](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-总界面.png)

教师可在录制过程中实时批注，也可在课后对视频进行时间轴批注：

![视频管理-老师批注](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-老师批注.png)

批注支持标记为"公开"（家长可见）或"内部"（仅教师可见）。

视频上传后，系统自动触发 AI 批注流水线：

![视频管理-AI-转文本和批注](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-AI-转文本和批注.png)

教师可对 AI 批注进行审核：批准、修改或拒绝。

#### 视频分发

教师审核批准后，点击「分发」按钮，系统自动匹配学员对应的家长，生成带签名的安全访问链接：

![视频管理-信息-分发](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-信息-分发.png)

系统通过微信或钉钉发送通知给家长。

### 3.3 教务端

#### 学员管理与分班

教务人员在后台管理学员信息，更新缴费状态并分配班级：

![学员管理](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理.png)

学员缴费后，教务将其分配到对应班级：

![学员管理-分班](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理-分班.png)

标记学员缴费状态：

![学员管理-标记已经收费](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理-标记已经收费.png)

### 3.4 管理员端

#### 用户管理

管理员管理系统用户（教师、教务账号）：

![用户管理](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/用户管理.png)

#### 批量管理

支持通过 Excel 批量导入用户、班级、学员、家长等基础数据：

![批量管理](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/批量管理.png)

#### 系统设置

**存储设置**：配置视频存储路径，支持本地磁盘、MinIO、阿里云 OSS

![系统设置-存储](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-存储.png)

**AI 设置**：配置 AI 服务参数，包括 whisper.cpp 模型和 Qwen API Key

![系统设置-AI](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-AI.png)

**通知设置**：配置微信/钉钉消息通知渠道

![系统设置-通知](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-通知.png)

---

## 四、技术架构

### 整体架构

录匣采用前后端分离架构：

- **前端**：Web 管理端（Vue/React）、微信小程序、钉钉小程序、Android App（Flutter/React Native）
- **后端**：RESTful API 服务，用户认证、业务逻辑、数据存储
- **AI 流水线**：whisper.cpp 本地语音转文本 + Qwen API 云端智能评测
- **存储层**：本地磁盘 / MinIO / 阿里云 OSS
- **通知层**：微信/钉钉消息推送

### 技术亮点

1. **AI 批注流水线**：视频上传后自动触发，无需人工干预
2. **多平台录制**：桌面端高质量录制 + Android 灵活录制
3. **安全分发**：签名 URL 保障家长访问安全
4. **批量导入**：Excel 模板降低 institutions 数据迁移成本

---

## 五、业务规模与约束

### 适用规模

- 小型培训机构（10-50 名学员）
- 中型培训机构（50-500 名学员）
- 大型培训机构（500+ 名学员，需分布式存储）

### 约束与限制

- AI 分析依赖 whisper.cpp 和 Qwen API 的可用性
- 视频存储容量取决于所选存储方案
- 微信小程序和钉钉小程序需提前完成企业认证

---

## 六、总结

录匣 Recxia 通过数字化手段，将高考面试培训机构的模拟面试全流程纳入统一平台管理，实现：

- **教务高效管理**：Excel 批量导入，一键分班
- **教师便捷录制**：PC/Android 双端支持，自动上传
- **AI 智能分析**：自动转录文本，生成教学评价
- **家长深度参与**：小程序实时查看视频与批注

系统核心价值：构建"排序→模拟→录制→AI分析→批注→分发→反馈→改进"的完整教学闭环，提升面试培训效果。
