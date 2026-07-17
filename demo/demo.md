# RecXia — Mock Interview Recording Management System Demo

[中文介绍](demo.zh.md)

![RecXia Logo](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/logo_256.png)

## 1. Product Overview

RecXia is an AI-powered mock interview recording management system designed for college entrance interview training institutions. It enables a complete teaching closed loop: Schedule → Simulate → Record → AI Analyze → Feedback → Improve.

### Core Values

| Value | Description |
|-------|-------------|
| Complete Loop | Covers the full workflow from enrollment to parent feedback |
| AI Empowerment | Automatic speech-to-text and intelligent evaluation |
| Multi-Platform | Web, desktop, Android, and mini-programs |
| Efficient Management | Excel batch import, one-click distribution |

### Applicable Roles

| Role | Core Functions | Access Method |
|------|----------------|---------------|
| Administrator | System maintenance, user management | Web browser |
| Academic Affairs | Enrollment, class assignment, payment status | Web browser |
| Teacher | Session creation, recording, annotation, distribution | Desktop app / Android App / Web |
| Student | Being recorded, no direct system interaction | — |
| Parent | Watch videos, view annotations, download | WeChat mini-program / DingTalk mini-program / H5 |

---

## 2. Business Process Overview

```
Parent enrollment / Academic Affairs enrollment → Confirm payment → Assign class → Assign teacher
    ↓
Teacher creates mock session → Adjust student order → Start recording (PC/Android)
    ↓
Video auto-upload → AI analysis generates annotations → Teacher reviews annotations
    ↓
Teacher distributes video → Parent receives notification → View video, annotations, download
```

| Phase | Owner | Key Actions |
|-------|-------|-------------|
| Enrollment & Payment | Academic Affairs | Student entry, class assignment, payment marking |
| Session Creation | Teacher | Select class, adjust order, start recording |
| Recording & Upload | Teacher | PC or Android recording, automatic upload |
| AI Analysis | System | Speech-to-text, generate evaluation |
| Review & Distribute | Teacher | Review annotations, one-click distribution |
| View & Feedback | Parent | View video and annotations via mini-program |

---

## 3. Role Details

### 3.1 Parent Portal

#### Parent Registration

Parents can self-register through the WeChat mini-program by filling in parent name, student name, and contact information:

![Mini-program parent registration input](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长注册输入.jpg)

Registration success message:

![Mini-program parent registration success](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长注册成功.jpg)

Parents can also log in via WebApp:

![WebApp parent login](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-登录.png)

#### Parent Video Viewing

Parents access the video viewing page through the received link:

![WebApp parent entry](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-家长入口.png)

View all mock interview videos of their child:

![WebApp student video list](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-学生视频列表.png)

Play video online and view AI-generated speech-to-text transcript:

![WebApp video preview and transcript](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-视频预览和语音转录文本.png)

![Mini-program transcript](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-语音转录.jpg)

Video player page displays teacher comments and AI analysis suggestions:

![WebApp teacher and AI annotations](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/webapp-教师和AI批注.png)

![Mini-program teacher annotation](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-教师批注.jpg)

Parents can click annotation timestamps to automatically jump to the corresponding position in the video.

Complete mini-program experience:

![Mini-program login](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-登录.jpg)

![Mini-program view recordings](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频.jpg)

![Mini-program watch video](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/小程序家长查看录制视频-看视频.jpg)

### 3.2 Teacher Portal

#### Launch Recording App

Teachers click the "Launch Recording" button on the Web side to invoke the native recording application:

![Mock practice launch app](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-启动模拟练习app.png)

#### Create Mock Interview Session

After launching the recording app, teachers create a mock interview session, select the class, and adjust the student order:

![Mock practice create session](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-创建模拟练习.png)

Creation success prompt:

![Mock practice create success](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-创建模拟练习成功.png)

#### Android Recording Flow

Teachers use Android phones for classroom recording, flexible and convenient:

**Step 1: Create practice session**

![Android create session](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-创建练习场次.jpg)

**Step 2: View session list**

![Android session list](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-场次列表.jpg)

**Step 3: Start recording**

![Android record](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制.jpg)

**Step 4: Recording in progress**

![Android recording](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制中.jpg)

**Step 5: Recording upload**

![Android recording upload](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-录制上传.jpg)

**Step 6: Upload video**

![Android upload](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-上传.jpg)

**Step 7: Upload success**

![Android upload success](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/android-模拟练习-上传成功.jpg)

#### Desktop Recording Interface

The desktop provides high-quality recording experience with clear display of current student, progress, and recording status:

![Mock practice recording interface](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制界面.png)

![Mock practice recording](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制中.png)

![Mock practice upload after recording](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟练习-录制完上传.png)

Complete mock interview recording system:

![Mock interview recording system](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/模拟面试录制系统.png)

#### Video Management & Annotation

Teachers view all recorded videos on the Web side, supporting filtering by session and student:

![Video management overview](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-总界面.png)

Teachers can annotate in real-time during recording or add timeline annotations after class:

![Video management teacher annotation](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-老师批注.png)

Annotations support marking as "Public" (visible to parents) or "Internal" (teachers only).

After video upload, the system automatically triggers the AI annotation pipeline:

![Video management AI transcript and annotation](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-AI-转文本和批注.png)

Teachers can review AI annotations: approve, modify, or reject.

#### Video Distribution

After teacher review and approval, click the "Distribute" button. The system automatically matches the student's parent and generates a signed secure access link:

![Video management info distribution](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/视频管理-信息-分发.png)

The system sends notifications to parents via WeChat or DingTalk.

### 3.3 Academic Affairs Portal

#### Student Management & Class Assignment

Academic staff manage student information in the backend, update payment status, and assign classes:

![Student management](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理.png)

After student payment, academic staff assign them to corresponding classes:

![Student management class assignment](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理-分班.png)

Mark student payment status:

![Student management payment marked](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/学员管理-标记已经收费.png)

### 3.4 Administrator Portal

#### User Management

Administrators manage system users (teacher, academic affairs accounts):

![User management](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/用户管理.png)

#### Batch Management

Support batch import of users, classes, students, parents, and other basic data via Excel:

![Batch management](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/批量管理.png)

#### System Settings

**Storage Settings**: Configure video storage path, supporting local disk, MinIO, Alibaba Cloud OSS

![System settings storage](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-存储.png)

**AI Settings**: Configure AI service parameters, including whisper.cpp model and Qwen API Key

![System settings AI](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-AI.png)

**Notification Settings**: Configure WeChat/DingTalk message notification channels

![System settings notification](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/demo/resources/系统设置-通知.png)

---

## 4. Technical Architecture

### Overall Architecture

RecXia adopts a front-end/back-end separated architecture:

- **Front-end**: Web management portal (Vue/React), WeChat mini-program, DingTalk mini-program, Android App (Flutter/React Native)
- **Back-end**: RESTful API services, user authentication, business logic, data storage
- **AI Pipeline**: whisper.cpp local speech-to-text + Qwen API cloud intelligent evaluation
- **Storage Layer**: Local disk / MinIO / Alibaba Cloud OSS
- **Notification Layer**: WeChat/DingTalk message push

### Technical Highlights

1. **AI Annotation Pipeline**: Automatically triggered after video upload, no manual intervention required
2. **Multi-Platform Recording**: Desktop high-quality recording + Android flexible recording
3. **Secure Distribution**: Signed URLs ensure secure parent access
4. **Batch Import**: Excel templates reduce data migration costs for institutions

---

## 5. Business Scale & Constraints

### Applicable Scale

- Small training institutions (10-50 students)
- Medium training institutions (50-500 students)
- Large training institutions (500+ students, distributed storage required)

### Constraints & Limitations

- AI analysis depends on availability of whisper.cpp and Qwen API
- Video storage capacity depends on chosen storage solution
- WeChat and DingTalk mini-programs require prior enterprise certification

---

## 6. Summary

RecXia digitizes the entire mock interview workflow for college entrance interview training institutions, enabling:

- **Efficient academic management**: Excel batch import, one-click class assignment
- **Convenient teacher recording**: PC/Android dual support, automatic upload
- **AI intelligent analysis**: Automatic transcription, generate teaching evaluation
- **Deep parent engagement**: Real-time video and annotation viewing via mini-programs

Core value: Build a complete teaching closed loop — Schedule → Simulate → Record → AI Analyze → Annotate → Distribute → Feedback → Improve — to enhance interview training effectiveness.
