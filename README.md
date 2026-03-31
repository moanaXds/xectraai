<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=E8724A&height=200&section=header&text=XectraAI&fontSize=80&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Know%20Exactly%20How%20Ready%20You%20Are&descAlignY=55&descAlign=50&descSize=20" width="100%"/>

<br/>

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-xectraai.netlify.app-E8724A?style=for-the-badge&logoColor=white)](https://xectraai.netlify.app)
[![GitHub Stars](https://img.shields.io/github/stars/moanaXds/xectraai?style=for-the-badge&color=E8724A)](https://github.com/moanaXds/xectraai/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/moanaXds/xectraai?style=for-the-badge&color=7BAE8A)](https://github.com/moanaXds/xectraai/network)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

<br/>

<img src="https://readme-typing-svg.demolab.com?font=Plus+Jakarta+Sans&weight=700&size=22&pause=1000&color=E8724A&center=true&vCenter=true&width=600&lines=AI-Powered+Exam+Prep+for+Pakistani+Students;Generate+Personalised+MCQs+Instantly;FAST+%7C+NUST+%7C+GIKI+%7C+COMSATS+Entry+Tests;Know+Exactly+How+Ready+You+Are+%F0%9F%9A%80" alt="Typing SVG" />

<br/><br/>

</div>

---

## What is XectraAI?

**XectraAI** is a free AI-powered exam preparation platform built specifically for **Pakistani university students**. It generates personalised, exam-level MCQs tailored to your selected university, subject, and difficulty in seconds.

Whether you're preparing for **FAST NU**, **NUST NET**, **GIKI**, or **COMSATS** entry tests, XectraAI builds a custom exam and tells you exactly where to improve.

---

## 🚀 Features

<table>
<tr>
<td width="50%">

### 🎯 Entry Test Preparation
Exam-calibrated MCQs for:
- **FAST NU** — Math, Physics, English, IQ
- **NUST NET** — All engineering subjects
- **GIKI** — Extremely analytical questions
- **COMSATS** — FSc syllabus aligned

</td>
<td width="50%">

### 📚 School & University Mode
- Grades 1–12 school exams
- University Year 1–4 courses
- Any subject, any topic
- MCQ, Written & Logic question types

</td>
</tr>
<tr>
<td width="50%">

### ⚡ Instant AI Generation
- Powered by **LLaMA 3.3 70B** via Groq
- Questions generated in under 10 seconds
- Difficulty spread: Easy → Medium → Hard
- Full explanations for every answer

</td>
<td width="50%">

### 📊 Detailed Results
- Score percentage with animated ring
- Correct / Wrong / Skipped breakdown
- Question-by-question review
- Shareable PDF report

</td>
</tr>
</table>

---

## 🛠️ Tech Stack

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)

</div>

| Layer | Technology |
|---|---|
| **Frontend** | Vanilla HTML, CSS, JavaScript |
| **AI Model** | LLaMA 3.3 70B via Groq API |
| **Backend** | Supabase Edge Functions (Deno) |
| **Auth** | Supabase Auth (Email + Google OAuth) |
| **Hosting** | Netlify |
| **Fonts** | Plus Jakarta Sans, Inter |

---

## 🏗️ Architecture

```
User Browser
     │
     ▼
index.html (Frontend)
     │
     │  POST /functions/v1/xectraai_function
     ▼
Supabase Edge Function (Deno)
     │
     │  Groq API — LLaMA 3.3 70B
     ▼
AI Question Generation
     │
     ▼
JSON Response → Rendered Exam
```

> **Security:** The Groq API key never touches the frontend. It lives exclusively inside the Supabase Edge Function.

---

## 📸 Screenshots

<div align="center">

| Landing Page | Exam Setup | Results |
|---|---|---|
| Clean animated hero | University + subject picker | Score ring + review |
<img width="1682" height="855" alt="image" src="https://github.com/user-attachments/assets/e69c9ef8-96df-4591-9289-bffe8d0b3f05" />
<img width="1541" height="823" alt="image" src="https://github.com/user-attachments/assets/0c1a4e84-1ad6-4af9-b055-901dd8566cda" />

</div>

---

## 🚦 Getting Started

### Option 1 — Just use it
Visit **[xectraai.netlify.app](https://xectraai.netlify.app)** — no installation needed.

### Option 2 — Run locally

```bash
# Clone the repo
git clone https://github.com/moanaXds/xectraai.git

# Open in VS Code
cd xectraai
code .

# Open index.html with Live Server
# Right click index.html → Open with Live Server
```

> **Note:** To generate questions locally, you'll need your own Groq API key and Supabase project. Update the endpoint URL and anon key in `index.html`.

---

## ⚙️ Environment Setup

To run your own instance:

1. Create a [Supabase](https://supabase.com) project
2. Create an Edge Function named `xectraai_function`
3. Add `GROQ_API_KEY` as a Supabase secret
4. Get a free [Groq API key](https://console.groq.com)
5. Update these values in `index.html`:

```js
const supabaseClient = createClient(
  'YOUR_SUPABASE_URL',
  'YOUR_SUPABASE_ANON_KEY'
);
```

---

## 🗺️ Roadmap

- [x] FAST, NUST, GIKI, COMSATS entry test prep
- [x] School (Gr 1–12) and University (Yr 1–4) modes
- [x] Supabase Auth — Email + Google OAuth
- [x] Shareable PDF results
- [x] Google Search Console indexing
- [ ] Question history & progress tracking
- [ ] Leaderboard between friends
- [ ] Mobile app (React Native)
- [ ] Urdu language support
- [ ] Teacher dashboard

---

## 👨‍💻 Author

<div align="center">

<img src="https://github.com/moanaXds.png" width="100" style="border-radius:50%"/>

**Muanna Hamid**
*Data Science Student @ FAST NUCES Islamabad*

[![GitHub](https://img.shields.io/badge/GitHub-moanaXds-181717?style=for-the-badge&logo=github)](https://github.com/moanaXds)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/moanaxds)

</div>

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=E8724A&height=120&section=footer&animation=fadeIn" width="100%"/>

**If XectraAI helped you — drop a ⭐ on the repo. It means a lot.**

</div>
