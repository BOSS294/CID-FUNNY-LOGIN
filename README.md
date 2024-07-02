# CID Funny Login

**CID-Themed Login System** 🎬🔐

This project presents a fun, CID-themed login system where users are entertained with iconic CID meme videos upon successful login. It offers a unique and engaging user experience by integrating CID-themed elements throughout the application.

## Features

- **🎭 CID-Themed:** Enjoy the nostalgic CID series with themed memes and videos.
- **🔐 Credential Check:** Validate login with predefined username and password.
- **📽️ Video Playback:** Plays a specific video on successful login.
- **⚠️ Custom Alerts:** Utilizes SweetAlert for custom, stylish pop-up messages.
- **🔊 Audio Control:** Plays background music with an option to pause.
- **📋 Session Management:** Manages user sessions to control video playback.
- **📱 Responsive Design:** Fully responsive, providing a seamless experience on all devices.
## Videos 
- Timelaspe of CID FUNNY LOGIN CREATION : 
- CID FUNNY LOGIN Full Video : 
## Images
![image](https://github.com/BOSS294/CID-FUNNY-LOGIN/assets/72921622/07872cde-d55f-4d3e-b5cd-7281e51c872e)

## Developed By 
- **MAYANK CHAWDHARI**
## Special Thanks to
- **Kishan Kumar**
- **Vedant**
## User Guide

### Predefined Credentials

- **Username:** Admin
- **Password:** 12345678

### Authentication and Video Playback

1. **Enter Credentials:** Input the predefined username and password.
2. **Play Video:** On successful login, a full-screen video will play.
3. **Session Management:** The user's authentication status is stored, allowing for conditional video playback.
4. **Redirect and Audio Control:** After the video ends, the user is redirected back, and any playing audio is stopped.

### Changing Authentication for Specific Videos

To play different videos based on authentication:

1. **Edit the Auth Variable:**
   In the JavaScript code, locate the `auth` variable. Set its value to 1 or 0 based on the condition.
   ```javascript
   const auth = 1; // or 0
   ```
2. **Specify Video Source:**
   Update the video source paths for different auth values.
   ```javascript
   if (auth === 1) {
       fullScreenVideo.src = '2.mp4'; // Path to video for auth = 1
   } else {
       fullScreenVideo.src = '1.mp4'; // Path to video for auth = 0
   }
   ```

## Implementation

### Custom Pop-Up Alerts

- **SweetAlert:** Stylish pop-up messages for user notifications.
  ```javascript
  Swal.fire({
      text: 'Please fill out all fields!',
      position: 'top-end',
      timerProgressBar: true,
      showConfirmButton: false,
      width: '250px',
      timer: 3000,
      backdrop: false
  });
  ```

### Full-Screen Video Playback

- **HTML Video Element:**
  ```html
  <video id="fullScreenVideo" autoplay controls>
      <source src="path/to/your/video-file.mp4" type="video/mp4">
      Your browser does not support the video tag.
  </video>
  ```
- **JavaScript to Handle Video Playback and Redirection:**
  ```javascript
  fullScreenVideo.addEventListener('ended', function() {
      stopAllAudio();
      window.location.href = 'login.html';
  });
  ```

- **Responsive Layout:**
  Ensures compatibility across various devices for a seamless user experience.

Enjoy the CID-themed login system and enhance your application's user engagement with iconic CID moments! 🎉🔐
