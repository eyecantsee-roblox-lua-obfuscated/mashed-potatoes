# 🥔 Mashed Potatoes

<div align="center">

![GitHub repo size](https://img.shields.io/github/repo-size/eyecantsee-roblox-lua-obfuscated/mashed-potatoes?style=for-the-badge&logo=github&color=5865F2)
![GitHub contributors](https://img.shields.io/github/contributors/eyecantsee-roblox-lua-obfuscated/mashed-potatoes?style=for-the-badge&logo=github&color=5865F2)
![GitHub stars](https://img.shields.io/github/stars/eyecantsee-roblox-lua-obfuscated/mashed-potatoes?style=for-the-badge&logo=github&color=5865F2)
![GitHub forks](https://img.shields.io/github/forks/eyecantsee-roblox-lua-obfuscated/mashed-potatoes?style=for-the-badge&logo=github&color=5865F2)
![License](https://img.shields.io/github/license/eyecantsee-roblox-lua-obfuscated/mashed-potatoes?style=for-the-badge&logo=mit&color=5865F2)

### *Meet. Chat. Connect. Date.*

A hybrid social matchmaking and real-time community hub built for speed, safety, and spontaneous online friendships.  (13+ / 17-)

---

### 🌐 Built With

![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
![.NET Core](https://img.shields.io/badge/.NET%208-%20512BD4.svg?style=for-the-badge&logo=dotnet&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

</div>

---

<details>
<summary><b>📌 Table of Contents (Click to Expand)</b></summary>

1. [About the Project](#-about-the-project)
2. [Key Features](#-key-features)
3. [Architecture & Tech Stack](#-architecture--tech-stack)
4. [Getting Started](#-getting-started)
   * [Prerequisites](#prerequisites)
   * [Installation & Setup](#installation--setup)
5. [Usage & Workflow](#-usage--workflow)
6. [Choosing a License](#-choosing-a-license)
7. [Contributing](#-contributing)
8. [License](#-license)

</details>

---

## 💡 About the Project

Traditional dating apps often feel transactional and exhausting, while community platforms like Discord can make one-on-one discovery daunting. **Mashed Potatoes** bridges the gap by combining intuitive profile discovery with rich, real-time messaging and voice spaces.  (Tinder x Discord)

* **Instant Discovery:** Swipe or browse active profiles based on mutual interests, gaming habits, or custom vibe tags.
* **Low-Pressure Communication:** Hop directly into real-time voice chats or initiate text chats without awkward formalities.
* **Fluid Relationship Modes:** Effortlessly switch between "Friends Only" and "Open to Dating" modes.
* **Security Measures:** No one under 13 or over 17 are allowed and we will check age identification before instantly ip and device banning them.  (Zero Chance of PDF Files)

---

## ✨ Key Features

* 🎴 **Match Card Swiping & Discovery Grid:** Dynamic matching engine powered by C# backend microservices.
* 💬 **Discord-Style Real-Time Messaging:** WebSockets & SignalR-powered channels with markdown support, custom emojis, and media sharing.
* 🎙️ **Voice & Audio Hubs:** Low-latency WebRTC voice rooms for casual group hangouts before moving to 1-on-1 DMs.
* 🏷️ **Dynamic Vibe Tags:** Smart interest matching across games, music, programming, and lifestyle.
* ⚡ **Icebreaker Mini-Games:** Interactive games inside chat rooms to break the silence instantly.
* 💾 **Setting To Save or Not Save Chat:** There is a setting to enable or disable text chats history from saving like snapchat to remain anonymous.

---

## 🛠️ Architecture & Tech Stack

```
               +---------------------------------------------------+
               |             React / Web Client Interface          |
               +---------------------------------------------------+
                                         |
                               (REST / WebSockets / SignalR)
                                         v
               +---------------------------------------------------+
               |             C# .NET Core Gateway API              |
               +---------------------------------------------------+
                       /                 |                 \
                      v                  v                  v
     +--------------------+   +-------------------+   +--------------------+
     | Matchmaking Engine |   | Real-Time Chat    |   | WebRTC Voice Core  |
     |   (C# / EF Core)   |   |   (SignalR / C#)  |   |  (Node / WebRTC)   |
     +--------------------+   +-------------------+   +--------------------+
               |                         |                      |
               +-------------------------+----------------------+
                                         v
                       +-----------------------------------+
                       |    PostgreSQL  /  Redis Cache     |
                       +-----------------------------------+
```

---

## 🚀 Getting Started

<details>
<summary><b>📋 Prerequisites</b></summary>

Ensure you have the following installed on your machine:
* [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
* [Node.js](https://nodejs.org/) (v18.0.0 or higher)
* [Docker Desktop](https://www.docker.com/products/docker-desktop/) (Optional, for easy DB provisioning)
* [Git](https://git-scm.com/)

</details>

<details>
<summary><b>🛠️ Installation & Setup (Step-by-Step)</b></summary>

### 1. Clone the repository
```bash
git clone https://github.com/your-username/mashed-potatoes.git
cd mashed-potatoes
```

### 2. Start Infrastructure (PostgreSQL & Redis)
```bash
docker-compose up -d
```

### 3. Setup Backend (C# / .NET Core)
```bash
cd backend/MashedPotatoes.API
dotnet restore
dotnet ef database update
dotnet run
```

### 4. Setup Frontend (React / TypeScript)
```bash
cd ../../frontend
npm install
npm run dev
```

</details>

---

## 🕹️ Usage & Workflow

1. **Setup your Profile:** Add your avatar, personal bio, and select your primary *Vibe Tags*.
2. **Select your Intention:** Set your status to **Friendship**, **Dating**, or **Open to Both**.
3. **Explore & Hang Out:** Browse match cards or join public voice lounges.
4. **Connect:** Chat instantly when mutual interest is confirmed!

---

## 📄 Choosing a License

For a social application fork like **Mashed Potatoes**, here are the three best options depending on your goals:

| License | Best Used For... | Key Feature |
| :--- | :--- | :--- |
| **MIT License** | Maximum adoption, fully open | Permissive; anyone can use, modify, or monetise your code with minimal restriction. |
| **GPL-3.0** | Open-source protection | Copyleft; any modified versions or forks **must** also remain open source. |
| **AGPL-3.0** | Hosted Web Applications | Strong copyleft; forces anyone hosting a modified version as a web service to release their source code. |

---

## 🤝 Contributing

Contributions make the open-source community an incredible place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the **MIT License**. See [`LICENSE`](./LICENSE) for more details.

## 🟢 App

This is a soon-to-be app on apple and android devices, it will currently be a open sourced localhost web-page until it's fully made and/or in-development.
