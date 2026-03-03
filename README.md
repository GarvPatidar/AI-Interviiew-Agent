
#  AI Smart Interview Platform


# 🎙️ InterviewIQ.AI – AI Smart Interview Platform

An AI-powered mock interview platform built using the MERN stack.  
It allows users to practice real-time AI-driven interviews, receive structured feedback, and track performance analytics.

---

## 🚀 Features

- 🔐 Google Authentication (JWT + Cookie-based Auth)
- 🤖 AI-Based Question Generation (Role + Experience + Resume Based)
- 🎤 Real-Time Voice Interview (Speech Recognition + AI Voice)
- 📊 AI Evaluation (Confidence, Communication, Correctness)
- 📄 Downloadable PDF Performance Report
- 💳 Razorpay Payment Integration
- 💰 Credit-Based Interview System
- 📈 Interview History & Analytics Dashboard

---

## 🏗️ Tech Stack

### Frontend
- React.js
- Redux Toolkit
- Tailwind CSS
- React Router
- SpeechSynthesis API
- Web Speech API

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- Multer (File Upload)
- pdfjs (Resume Parsing)

### AI Integration
- OpenRouter API (GPT-4o-mini)

### Payment
- Razorpay SDK
- HMAC SHA256 Signature Verification

---

## 🔐 Authentication Flow

1. User logs in via Google.
2. Backend verifies/creates user.
3. JWT token generated.
4. Token stored in HTTP-only cookie.
5. Protected routes verified using middleware.

---

## 🤖 AI Interview Flow

1. User selects role or uploads resume.
2. Resume parsed using PDF.js.
3. AI generates 5 structured interview questions.
4. Credits deducted (50 per interview).
5. User answers via voice or text.
6. AI evaluates answer and returns:
   - Confidence
   - Communication
   - Correctness
   - Final Score
   - Short Feedback
7. Final analytics calculated.
8. User can download structured PDF report.

---

## 💳 Payment Flow

1. User selects plan.
2. Backend creates Razorpay order.
3. Razorpay checkout opens.
4. Payment signature verified using HMAC SHA256.
5. Credits added to user account.

---

## 🗄️ Database Design

### User
- name
- email
- credits

### Interview
- userId (ref)
- role
- experience
- mode
- resumeText
- questions[]
- finalScore
- status

### Payment
- userId
- planId
- amount
- credits
- razorpayOrderId
- status

---

## 🧠 Challenges Faced

- Handling strict JSON responses from AI
- Managing mic & AI speech synchronization
- Secure payment verification
- Credit management consistency
- Resume text extraction & normalization

---

## 📦 Installation & Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/interviewiq-ai.git
cd interviewiq-ai
````

### 2️⃣ Install Dependencies

#### Backend

```bash
cd backend
npm install
```

#### Frontend

```bash
cd frontend
npm install
```

---

### 3️⃣ Environment Variables (Backend)

Create a `.env` file:

```env
PORT=8000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
OPENROUTER_API_KEY=your_openrouter_key
RAZORPAY_KEY_ID=your_key
RAZORPAY_KEY_SECRET=your_secret
```

---

### 4️⃣ Run Application

#### Backend

```bash
npm run dev
```

#### Frontend

```bash
npm run dev
```

---

## 📈 Future Improvements

* Emotion detection using webcam
* AI difficulty personalization
* Admin analytics dashboard
* Redis caching
* Microservice-based scaling

---

## 💡 Learning Outcome

This project demonstrates:

* Full-stack MERN development
* Secure authentication architecture
* AI integration with prompt engineering
* Real-time speech interaction
* Payment gateway integration
* Scalable database design

---

## 👨‍💻 Author

Garv Patidar
MERN Stack Developer




