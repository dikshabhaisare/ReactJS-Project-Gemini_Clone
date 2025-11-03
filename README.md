# 🌟 Gemini Clone (AI Chat App)

A fully functional **Gemini AI Clone** built using **React + Vite** that connects to the **Google Gemini API** to provide real-time AI chat responses.  
It mimics the interface and functionality of Google’s Gemini web app — with a modern, responsive UI.

---

## 🚀 Features

✅ Real-time AI Chat using Gemini API  
✅ Beautiful UI with React + Tailwind CSS  
✅ Context API for global state management  
✅ Fully Responsive (Mobile, Tablet, Desktop)  
✅ Loader animation while AI processes response  
✅ Supports Markdown & multi-line responses  
✅ Error handling for API rate limits and invalid keys  

---

## 🧩 Tech Stack

- ⚛️ **React + Vite** – frontend framework & bundler  
- 💅 **Tailwind CSS** – modern styling  
- 🧠 **Google Generative AI SDK (@google/genai)** – for Gemini API  
- 🔄 **Context API** – state management  
- 📦 **Axios / Fetch** – for API requests  

---

## 🗂️ Project Structure

src/
├── components/
│ ├── Navbar.jsx
│ ├── ChatBox.jsx
│ ├── Loader.jsx
│
├── context/
│ └── Context.jsx
│
├── config/
│ └── gemini.js
│
├── pages/
│ ├── Main.jsx
│
├── App.jsx
├── main.jsx
└── index.css

yaml
Copy code

---

## ⚙️ Installation

1️⃣ Clone the repository  
```bash
git clone https://github.com/your-username/gemini-clone.git
2️⃣ Navigate into the project

bash
Copy code
cd gemini-clone
3️⃣ Install dependencies

bash
Copy code
npm install
4️⃣ Create a .env file in the root and add your Gemini API Key

ini
Copy code
VITE_GEMINI_API_KEY=your_api_key_here
5️⃣ Start the development server

bash
Copy code
npm run dev
🔑 How to Get Gemini API Key
Visit Google AI Studio

Sign in with your Google account

Go to Get API key → Create API Key

Copy the key and paste it into .env

🧠 Example Code Snippet (API Integration)
javascript
Copy code
import { GoogleGenAI } from "@google/genai";

const API_KEY = import.meta.env.VITE_GEMINI_API_KEY;
const genAI = new GoogleGenAI({ apiKey: API_KEY });

export async function runChat(prompt) {
  try {
    const result = await genAI.models.generateContent({
      model: "gemini-2.0-flash-exp",
      contents: [{ role: "user", parts: [{ text: prompt }] }],
    });
    return result.response.text();
  } catch (error) {
    console.error("❌ Gemini API Error:", error);
    return "Error fetching response. Please try again.";
  }
}
🌐 Deployment
🔸 Deploy on Vercel
Push your code to GitHub

Go to https://vercel.com/

Import your repository

Add environment variable:

VITE_GEMINI_API_KEY=your_api_key_here

Click Deploy 🎉

🖼️ Preview
Chat UI	Responsive View
	

💡 Future Enhancements
🔊 Voice input and response

📚 Conversation history saving

🌗 Dark / Light mode toggle

💬 Multiple chat tabs

🧑‍💻 Author
Deeksha Bhaisare
✨ Passionate Frontend Developer
📧 Reach me on LinkedIn

🪪 License
This project is licensed under the MIT License – free to use and modify.
