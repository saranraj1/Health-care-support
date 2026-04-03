# MedReach - Healthcare Support Portal 🏥💚

Welcome to **MedReach**! This is a dynamic, AI-powered web platform designed to bridge the gap between underserved communities and healthcare resources. 

## 🌍 The NGO Use-Case
In many developing regions, accessing basic healthcare guidance is incredibly difficult. Clinics are far, specialists are expensive, and basic health questions go unanswered, leading to worse health outcomes. 

MedReach solves this by acting as a digital bridge for NGOs. It provides:
1. **A patient registration portal** to connect individuals directly to local medical volunteers and resources.
2. **A volunteer portal** for doctors, nurses, and students to offer their time and expertise.
3. **Curated health resources and clinic maps**, making navigation to physical care incredibly simple.

## 🤖 The AI Idea
The core of this application is an **intelligent, voice-enabled AI Chatbot** operating as a 24/7 frontline medical assistant. Powered by Groq and the LLaMA 3.3 model, the AI is prompted to instantly answer health FAQs, guide users through basic care (like maternal issues or first aid), and specifically detect when to redirect someone to an emergency hotline (like 108 in India). It serves as a triage system that reduces the burden on human volunteers while giving patients immediate support in multiple languages.

## 💻 Tech Stack
- **Frontend**: HTML5, Vanilla JavaScript, CSS3 (No Frameworks)
- **AI Processing**: Groq REST API (LLaMA-3.3-70b-versatile model)
- **APIs**: Web Speech API (Native browser voice-to-text functionality)
- **Deployment**: Vercel (or any static host)
- **Storage**: Browser `localStorage` (for theming and chat caching)

## 📄 Why a Single HTML File?
You might notice that the entire application—HTML, CSS, and thousands of lines of JavaScript logic—all lives inside `index.html`.

There is a very specific reason for this constraint: **Maximum Accessibility & Zero-Friction Deployment.**

By keeping everything in a self-contained, single HTML file:
- **No Build Steps**: You don't need `npm`, Node.js, Webpack, or a local server to run this. Just double-click the file, and it opens instantly in any browser.
- **Portability**: Want to share the app with a local clinic that has poor internet? Put it on a USB drive. It will run completely fine entirely offline (except for the AI chatbot).
- **Easy Auditing**: It shows that robust UI engineering, state management, and API integrations *can* be done with raw vanilla code without relying on bloated frameworks.

## ✨ Features
- **Voice Dictation**: Uses native Web Speech API so users can simply *talk* to the AI instead of typing.
- **Dark Mode**: Persists using local storage.
- **Groq AI Integration**: Native REST API calls to Groq's high-speed inference engine for real-time text generation, formatted with markdown.
- **Native Form Validations**: HTML5 form validations triggered seamlessly without jumping the gun.
- **Caching**: Chat history is persisted and fetched dynamically on reload to give a continuous experience.

## 🚀 How to use
1. Just open the live Vercel URL, or double-click `index.html` to open it locally in your browser.
2. If you want to use the AI chatbot, open the file in your code editor, find the `sendMsgText` function, and replace `'YOUR_API_KEY'` with a real Groq API key.

---
*Built with ❤️ for accessible healthcare.*
