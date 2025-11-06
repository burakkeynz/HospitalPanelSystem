# Hospital Panel System
---
An application that enables doctors, technisians and nurses to comminucate with each other at shifts on a single app. It includes WhatsApp style chatting via SocketIO, Discord style audio/video call, an AI assistant at the right side of page implemented with Gemini 2.5's API key and session logs of AI assistant and user chats.

> **Tech stack:** React, WebRTC, SocketIO, FastAPI, AudioWorklet
> **Status:** Can run on locally with SSL Certificate, not deployed

---

## App Overview

- **Flow:** A doctor/nurse or technician can log in via selecting Turkish or English, dark or light theme for app preferences of them. If they don't have an account they can create an account. After succesfully log in, a user can chat with other colleageus of his/her live. Can ask questions to his/her AI assistant about any topics, especially on their profession. Can save the log of the chat for later review or recheck if needed. Can audio/video call of their colleague for meetings (this meeting is recorded with AudioWorklet, and saved after finishing the meeting)
- **Goal:** Making shifts easy for meet-ups, chats and take an assistant for regular work days.

*(This is an overview of the project.)* 

---

## High level project struct 

```
CizgiTekProj/
  backend/
    alembic.ini
    database.py
    globals.py
    main.py
    models.py
    alembic/
      env.py
      versions/
        2eb805ef47d3_adding_call_id_to_sessionlogs.py
        ...
    certs/
    fastapienv/
    routers/
      auth.py
      chatlogs.py
      conversations.py
      files.py
      gemini.py
      patients.py
      prompts.py
      sessionlogs.py
      sessions.py
      upload.py
      users.py
    utils/
      aws_s3.py
      chat.py
      security.py

  frontend/
    package.json
    package-lock.json
    README.md
    public/
      index.html
      pcm-worklet.js
    src/
      App.js
      api.js
      index.css
      index.js
      assets/
      components/
        ActiveCall.jsx
        ActiveCallOverlay.jsx
        AppearanceSettings.jsx
        Assistant.jsx
        AuthLoadingSplash.jsx
        CallModal.jsx
        CardiologyCard.jsx
        Chat.jsx
        ChatDetail.jsx
        ChatLogDetail.jsx
        Dashboard.jsx
        FilePreviewModal.jsx
        Goodbye.jsx
        LanguageContext.jsx
        Login.jsx
        Sessions.jsx
        Settings.jsx
        ThemeContext.jsx
        UserInfoCard.jsx
      hooks/
        useAuthCheck.jsx
      store/
        callSlice.js
        chatSlice.js
        index.js
      utils/
        webrtc.js

```

---
## License

This project is under MIT License.
