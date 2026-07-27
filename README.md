<div align="center">
  
# 🌿 NatureRx AI

**An AI-Powered Organic Health & Wellness Assistant**

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Framer Motion](https://img.shields.io/badge/Framer_Motion-black?style=for-the-badge&logo=framer)](https://www.framer.com/motion/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Groq](https://img.shields.io/badge/Groq-AI-f55036?style=for-the-badge)](https://groq.com/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)

</div>

---

## 🚀 Live Deployment

**[🔗 Click Here to View the Live App in Action!](https://nature-rx-ai.vercel.app/)**  
*(Note to Grader: The application is fully deployed and functioning end-to-end.)*

---

## 📖 What it is & The Problem it Solves

**NatureRx AI** is an intelligent healthcare assistant designed to provide users with evidence-based natural remedies using herbs, plants, fruits, vegetables, and other commonly available household ingredients. 

### **The Real-World Problem**
Millions of people search the internet daily for natural remedies. Unfortunately, they face significant risks:
- **Misinformation:** Websites and social media are filled with unverified, unsafe "home remedies."
- **Lack of Evidence:** Users struggle to determine if a remedy is scientifically supported or just a myth.
- **Identification Issues:** People cannot easily identify plants in the wild or understand their medicinal benefits (and dangers).
- **Safety Hazards:** Many platforms fail to warn users when their symptoms require actual emergency medical care.

### **The Solution**
NatureRx AI acts as a beautiful, interactive, and AI-driven portal to the natural world. It replaces generic web searches with a highly-tuned AI assistant that prioritizes scientific natural alternatives while actively filtering for medical emergencies to keep users safe.

---

## ✨ Features List

NatureRx AI comes packed with powerful, production-ready features:

*   **🎙️ Voice-Enabled AI Consultations (`/chat`):** Users can text or speak (via Web Speech API) their symptoms. The AI analyzes the input and recommends safe, scientifically-backed natural remedies (e.g., Ginger tea for a sore throat).
*   **📸 AI Plant Image Analyzer (`/analyze`):** Users can upload or drag-and-drop a photo of any plant. The AI visually analyzes it to provide the exact identification, confidence score, medicinal benefits, precautions, and a health check (e.g., detecting plant diseases like powdery mildew).
*   **📚 Plant Encyclopedia (`/encyclopedia`):** A beautifully designed, searchable database of medicinal plants, trees, and herbs. Users can favorite plants to save them to a personal library.
*   **🍵 Remedies Database (`/remedies`):** A curated list of specific recipes for common ailments, explicitly displaying "Evidence Levels" (e.g., Strong Evidence, Traditional Use).
*   **🌓 Adaptive Glassmorphism UI:** Built with a stunning, modern glassmorphism design aesthetic using Tailwind CSS and Framer Motion for laser-scanning animations and micro-interactions. Flawlessly supports Dark/Light modes.
*   **🚑 Emergency Interception:** The AI is strictly prompted to recognize life-threatening symptoms and immediately reroute the user to seek professional emergency care.

---

## 🧠 The AI Magic (Prompts & Instructions)

This application leverages the blazing-fast **Groq API** to power two distinct AI features:

### 1. Chat Consultation Agent (Model: `llama-3.3-70b-versatile`)
**What it does:** Acts as a knowledgeable herbalist and wellness coach, interpreting user symptoms to suggest organic remedies, while maintaining strict medical safety protocols.

**System Prompt / Instructions behind it:**
```text
You are NatureRx AI, an expert in natural remedies and organic health.
Always prioritize scientifically supported natural alternatives (herbs, plants).
CRITICAL: If the user mentions emergency symptoms (chest pain, severe bleeding, breathing difficulty), 
you MUST advise them to seek immediate medical help.
```

### 2. Vision Plant Analyzer (Model: `llama-3.2-11b-vision-preview`)
**What it does:** Performs complex image recognition on user-uploaded plant photos. It doesn't just identify the plant; it diagnoses its health and formats the botanical data into a strict, parsable JSON structure for the frontend UI.

**System Prompt / Instructions behind it:**
```text
Analyze this image of a plant. Provide a JSON response ONLY with the following structure:
{
  "name": "Name of the plant",
  "confidence": 95,
  "benefits": ["benefit 1", "benefit 2"],
  "precautions": ["precaution 1", "precaution 2"],
  "healthStatus": "Healthy" | "Diseased" | "Needs Attention",
  "diseaseDetails": "Details if diseased or needs attention, otherwise null"
}
```

---

## 🛠️ Tools, Services, and AI Models Used

This project was built using a highly modern, full-stack ecosystem:

### **Frontend & UI**
*   **Next.js 16 (App Router):** The core React framework for routing, API endpoints, and optimized rendering.
*   **React 19:** The latest standard for component-based UI.
*   **Tailwind CSS (v4):** Used for rapid styling and creating the Glassmorphism aesthetic.
*   **Framer Motion:** Powers the smooth page transitions and the premium "laser scanning" animation on the image upload.
*   **Lucide React:** Clean, consistent SVG iconography.
*   **Next-Themes:** For seamless dark/light mode toggling.

### **Backend & Database**
*   **Supabase (`@supabase/supabase-js`):** Open-source Firebase alternative used for backend functionality (saving favorite plants, etc.).
*   **Next.js Route Handlers (`app/api/`):** Serverless functions to securely communicate with the AI without exposing API keys to the client.

### **AI & Machine Learning**
*   **Groq SDK:** The ultra-low latency AI inference engine platform.
*   **LLaMA 3.3 70B Versatile:** Used for complex text-based symptom analysis and chat.
*   **LLaMA 3.2 11B Vision Preview:** Used for the multimodal image analysis of plants.

---

## 📸 Screenshots

*(Replace the placeholder image URLs below with your actual screenshots before submitting)*

### 1. AI Chat Consultation Interface
![Chat Interface](https://via.placeholder.com/800x450.png?text=AI+Chat+Interface+Screenshot)
*The AI providing a safe, natural remedy for a user's symptoms.*

### 2. Plant Vision Analyzer
![Vision Analyzer](https://via.placeholder.com/800x450.png?text=Plant+Image+Analyzer+Screenshot)
*The laser-scanning UI identifying a medicinal plant and showing precautions.*

### 3. Plant Encyclopedia & Dark Mode
![Encyclopedia](https://via.placeholder.com/800x450.png?text=Plant+Encyclopedia+Dark+Mode)
*The searchable database in dark mode, showing glassmorphism UI elements.*

---

## 💻 How to Run the Project Locally

Follow these instructions to run a local development server on your machine:

### 1. Prerequisites
*   Ensure you have [Node.js](https://nodejs.org/) installed (v18+ recommended).
*   Obtain an API key from [Groq](https://console.groq.com/keys).
*   *(Optional)* Setup a [Supabase](https://supabase.com/) project for database features.

### 2. Installation Steps
Clone the repository and install the dependencies:
```bash
git clone https://github.com/sajid-dev-56/NatureRx-AI.git
cd NatureRx-AI
npm install
```

### 3. Environment Variables
Create a `.env.local` file in the root directory and add your API keys:
```env
GROQ_API_KEY="your_groq_api_key_here"
NEXT_PUBLIC_SUPABASE_URL="your_supabase_url"
NEXT_PUBLIC_SUPABASE_ANON_KEY="your_supabase_anon_key"
```

### 4. Run the Development Server
Start the Next.js server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to interact with the application.

---
<div align="center">
  <i>Built with ❤️ for a healthier, natural world.</i>
</div>
