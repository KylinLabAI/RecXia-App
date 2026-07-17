# RecXia — User Manual

[中文介绍](user_manual.zh.md)

![RecXia Logo](https://raw.githubusercontent.com/KylinLabAI/RecXia-App/master/user_manual/resources/logo_256.png)

## Introduction

Welcome to RecXia. This manual guides you through every feature, organized by what you want to accomplish.

## Administrator Guide

### Getting Started

#### Task: System Setup

**Prerequisites:**
- Server environment prepared
- Storage backend configured (local disk, MinIO, or Alibaba Cloud OSS)

**Steps:**

1. Log in to the RecXia Web admin panel
   - You will see: Dashboard with system overview

2. Navigate to System Settings
   - Configure storage path and credentials
   - Configure AI service parameters (whisper.cpp model path, Qwen API Key)
   - Configure WeChat/DingTalk notification channels

3. Save settings and verify connection
   - You will see: Green status indicators for all services

**Expected result:** All system services show healthy status.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Storage connection failed | Check credentials and network access |
| AI service unreachable | Verify API key and model path |

### Daily Operations

#### Task: User Management

**Prerequisites:**
- Administrator access

**Steps:**

1. Go to User Management page
   - You will see: List of existing users

2. Add individual users or use Batch Import
   - Download Excel template
   - Fill in user data (teachers, academic staff)
   - Upload file

3. Assign roles to users
   - You will see: Updated user list with roles

**Expected result:** Users can log in with assigned roles.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Import fails | Check Excel format matches template |
| User cannot log in | Verify username and role assignment |

### Troubleshooting

#### Task: System Maintenance

**Steps:**

1. Monitor system status dashboard
2. Check storage usage and clean up if needed
3. Review notification delivery logs

## Academic Affairs Guide

### Getting Started

#### Task: Student Enrollment

**Prerequisites:**
- Academic Affairs role assigned
- Class structures created

**Steps:**

1. Access Student Management page
   - You will see: Student list with enrollment status

2. Add students individually or via batch import
   - Fill student name, parent contact, intended class

3. Mark payment status
   - You will see: Payment status updated

4. Assign students to classes
   - You will see: Class rosters updated

**Expected result:** Students are enrolled and assigned to classes.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Duplicate student entries | Merge or delete duplicates in management page |
| Class assignment error | Reassign via edit function |

## Teacher Guide

### Getting Started

#### Task: Launch Recording Session

**Prerequisites:**
- Teacher role assigned
- Classes and students configured
- Recording app installed (desktop or Android)

**Steps:**

1. Log in to Web management portal
   - You will see: Teacher dashboard

2. Click "Launch Recording App" to open native recorder
   - Or use Android app directly

3. Create a new mock interview session
   - Select class
   - Adjust student order if needed
   - Confirm creation

4. Start recording when student is ready
   - You will see: Recording interface with timer and controls

5. Stop recording and upload video
   - You will see: Upload progress and confirmation

**Expected result:** Video uploaded and available in video management.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Recording app won't launch | Check browser permissions for protocol handlers |
| Upload fails | Check network and storage configuration |
| Android app crashes | Update to latest version |

### Daily Operations

#### Task: Video Management

**Prerequisites:**
- Recorded videos available

**Steps:**

1. Go to Video Management page
   - You will see: All recorded videos with filters

2. Select a video to review
   - Play video with timeline

3. Add annotations at specific timestamps
   - Type annotation text
   - Set visibility: Public (parents) or Internal (teachers only)

4. Review AI-generated transcript and annotations
   - Approve, modify, or reject AI suggestions

**Expected result:** Video has accurate teacher and AI annotations.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| AI transcript inaccurate | Manually edit or reprocess with different settings |
| Annotation not saving | Refresh page and retry |

#### Task: Distribute Video to Parents

**Prerequisites:**
- Video reviewed and annotated
- Student has linked parent account

**Steps:**

1. Open video details page
2. Click "Distribute" button
   - System generates signed access link
   - Notification sent to parent via WeChat/DingTalk

3. Confirm distribution
   - You will see: Distribution status updated

**Expected result:** Parent receives notification and can access video.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Parent not notified | Check notification channel settings |
| Link expired | Redistribute to generate new link |

## Parent Guide

### Getting Started

#### Task: Register and Access Videos

**Prerequisites:**
- Student enrolled by institution
- WeChat or DingTalk app installed (for mini-program)

**Steps:**

1. Receive registration link from institution
   - Or open WeChat/DingTalk mini-program

2. Fill in parent information
   - Parent name, student name, contact
   - Submit registration

3. Wait for institution approval
   - You will see: Registration success message

4. Access video list when notified
   - View all student's mock interview videos

**Expected result:** Parent can view videos, transcripts, and annotations.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Registration pending | Contact institution to approve |
| Cannot open link | Use supported browser or mini-program |

### Daily Operations

#### Task: Review Video and Feedback

**Steps:**

1. Open video from list
   - Video player loads with transcript panel

2. Play video and read AI transcript
   - Click transcript lines to jump to timestamp

3. Read teacher and AI annotations
   - Click annotation timestamps to jump to relevant moment

4. Download video if needed
   - Use download button (if enabled by institution)

**Expected result:** Full understanding of student's performance and feedback.

## Shared Tasks

### Login

**Steps:**

1. Open RecXia portal or app
2. Enter username and password
3. Click Login

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Forgot password | Contact administrator to reset |
| Account locked | Wait 30 minutes or contact administrator |

### Settings

**Steps:**

1. Go to Profile/Settings page
2. Update personal information
3. Change password if needed
4. Save changes

## Appendix

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Space | Play/Pause video |
| Left Arrow | Rewind 5 seconds |
| Right Arrow | Forward 5 seconds |

### Glossary

| Term | Definition |
|------|------------|
| Mock Interview | Simulated interview session for practice |
| Annotation | Comment attached to a specific video timestamp |
| AI Transcript | Automatically generated text from speech |
| Distribution | Sending video access to parents |
