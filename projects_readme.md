# Healthcare Assistant Web Application

A comprehensive healthcare web application that provides various medical assistance features to help users manage their health and get quick medical insights.

## 🌟 Features

- **Disease Prediction**: AI-powered disease prediction based on symptoms
- **Symptom Checker**: Interactive symptom assessment tool
- **Health Chat**: Real-time chat interface for medical queries powered by Gemini AI
- **Medication Management**: Track and manage your medications
- **User Authentication**: Secure login and registration system
- **CAPTCHA Security**: Enhanced security with CAPTCHA verification
- **Responsive Design**: Works seamlessly across all devices

## 🚀 Tech Stack

This project is built with modern technologies:

- **Frontend Framework**: React with TypeScript
- **Build Tool**: Vite
- **UI Components**: shadcn/ui
- **Styling**: Tailwind CSS
- **Backend Services**: Supabase
- **AI Integration**: Google's Gemini AI
- **Authentication**: Supabase Auth

## 💻 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or Bun package manager
- Supabase account for backend services

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd HCI-Project
```

2. Install dependencies:
```bash
# Using npm
npm install

# Using Bun
bun install
```

3. Set up environment variables:
Create a `.env` file in the root directory and add your Supabase credentials:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Start the development server:
```bash
npm run dev
# or
bun run dev
```

Visit `http://localhost:5173` to see the application running.

## 📁 Project Structure

- `/src` - Main application source code
  - `/components` - Reusable UI components
  - `/contexts` - React context providers
  - `/hooks` - Custom React hooks
  - `/integrations` - Third-party service integrations
  - `/pages` - Application pages/routes
  - `/lib` - Utility functions and configurations

## 🔒 Security Features

- Secure authentication using Supabase
- CAPTCHA verification for enhanced security
- Protected routes and API endpoints
- Secure data storage and transmission

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 📧 Contact

For any queries or support, please open an issue in the repository.

- email: cs22b1061@iiitdm.ac.in
- phone: 6301179024

----------
 # Interview Prep - AI-Powered Mock Interview Platform

A modern web application that helps users practice and improve their interview skills through AI-powered mock interviews with real-time voice interaction and detailed feedback analysis.

## 🌟 Features

- **AI Voice Interviews**: Practice interviews with an AI interviewer using natural voice conversations powered by Vapi AI
- **Personalized Interview Generation**: Create custom interviews tailored to specific roles, tech stacks, and experience levels
- **Real-time Feedback**: Get instant AI-generated feedback on communication skills, technical knowledge, problem-solving abilities, and more
- **Interview Library**: Access interviews created by other users for additional practice opportunities
- **Comprehensive Analytics**: Receive detailed performance breakdowns with scores across multiple categories
- **Secure Authentication**: Firebase-powered authentication system for user management

## 🚀 How It Works

### User Flow

1. **Sign Up/Sign In**: Create an account or log in to access the platform
2. **Dashboard**: View two main sections:
   - **Your Interviews**: Interviews you've created and can retake
   - **Take an Interview**: Interviews created by other users available for practice
3. **Start Interview**: Create a new interview by specifying:
   - Job role
   - Experience level
   - Tech stack
   - Interview type (technical/behavioral focus)
   - Number of questions
4. **AI Interview Session**: Engage in a real-time voice conversation with the AI interviewer
5. **Receive Feedback**: Get comprehensive AI-generated feedback including:
   - Overall score (0-100)
   - Category-wise performance analysis
   - Strengths identification
   - Areas for improvement
   - Final assessment

### Interview Types

- **Your Interviews**: Interviews you've created based on your preferences - perfect for practicing specific roles or technologies
- **Take an Interview**: Pre-created interviews by other users - great for exploring different interview scenarios and challenges

## 🛠️ Tech Stack

- **Framework**: Next.js 16 with React 19
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Authentication**: Firebase Authentication
- **Database**: Firebase Firestore
- **AI Integration**: 
  - Vapi AI for voice conversations
  - Google Gemini 2.5 Flash for interview generation and feedback
- **Voice Features**: 
  - Deepgram for transcription
  - ElevenLabs for AI voice
- **Form Management**: React Hook Form with Zod validation
- **UI Components**: Radix UI primitives with custom styling

## 📋 Prerequisites

- Node.js 20+ 
- npm/yarn/pnpm
- Firebase project with Firestore and Authentication enabled
- Vapi AI account and API keys
- Google AI Studio API key

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SVPraveen1/Interview_prep.git
   cd mock_interview_app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   # Firebase Client Configuration
   NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
   NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
   NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

   # Firebase Admin
   FIREBASE_ADMIN_PROJECT_ID=your_admin_project_id
   FIREBASE_ADMIN_CLIENT_EMAIL=your_admin_client_email
   FIREBASE_ADMIN_PRIVATE_KEY=your_admin_private_key

   # Vapi AI
   NEXT_PUBLIC_VAPI_PUBLIC_KEY=your_vapi_public_key
   NEXT_PUBLIC_VAPI_WORKFLOW_ID=your_vapi_workflow_id

   # Google AI
   GOOGLE_GENERATIVE_AI_API_KEY=your_google_ai_api_key
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Project Structure

```
├── app/
│   ├── (auth)/              # Authentication routes
│   │   ├── sign-in/
│   │   └── sign-up/
│   ├── (root)/              # Protected routes
│   │   ├── page.tsx         # Dashboard
│   │   └── interview/
│   │       ├── page.tsx     # Interview creation
│   │       └── [id]/
│   │           ├── page.tsx         # Interview session
│   │           └── feedback/
│   │               └── page.tsx     # Feedback display
│   └── api/
│       └── vapi/
│           └── generate/    # Interview generation endpoint
├── components/              # React components
│   ├── Agent.tsx           # Voice interview component
│   ├── AuthForm.tsx        # Authentication form
│   ├── InterviewCard.tsx   # Interview display card
│   └── ui/                 # UI primitives
├── lib/
│   ├── actions/            # Server actions
│   │   ├── auth.action.ts
│   │   └── general.action.ts
│   └── vapi.sdk.ts         # Vapi SDK integration
├── firebase/               # Firebase configuration
│   ├── admin.ts
│   └── client.ts
└── types/                  # TypeScript definitions
```

## 🎯 Key Features Explained

### Interview Generation
The AI generates personalized interview questions based on:
- **Role**: Software Engineer, Product Manager, Data Scientist, etc.
- **Level**: Junior, Mid-level, Senior
- **Tech Stack**: React, Node.js, Python, AWS, etc.
- **Type**: Technical-focused or Behavioral-focused
- **Amount**: Number of questions (customizable)

### Feedback System
After completing an interview, users receive detailed feedback including:
- **Communication Skills**: Clarity, articulation, and structured responses
- **Technical Knowledge**: Understanding of key concepts
- **Problem Solving**: Analytical thinking and solution approach
- **Cultural Fit**: Alignment with professional expectations
- **Confidence and Clarity**: Overall delivery and engagement

Each category is scored from 0-100 with specific comments and recommendations.

## 🔒 Security

- Firebase Authentication for secure user management
- Server-side authentication verification
- Protected routes using Next.js middleware
- Environment variables for sensitive data
- Firestore security rules (configure in Firebase Console)

## 📱 Responsive Design

The application is fully responsive and optimized for:
- Desktop browsers
- Tablets
- Mobile devices

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 👤 Author

**Praveen**
- GitHub: [@SVPraveen1](https://github.com/SVPraveen1)

## 🙏 Acknowledgments

- [Vapi AI](https://vapi.ai) for voice conversation capabilities
- [Google Gemini](https://ai.google.dev/) for AI-powered interview generation and feedback
- [Firebase](https://firebase.google.com/) for authentication and database
- [Next.js](https://nextjs.org/) for the React framework
- [Vercel](https://vercel.com/) for hosting platform

## 📞 Support

For support, questions, or feedback, please open an issue in the GitHub repository.

---

Made with ❤️ for interview preparation

------

# Sensai AI 🤖

  

> An intelligent AI-powered learning platform that revolutionizes personal education through adaptive learning and real-time feedback.


[![Node.js Version](https://img.shields.io/badge/node-%3E%3D%2016.0.0-brightgreen)](https://nodejs.org/)
  

## 🎯 Overview

  

Sensai AI is a cutting-edge learning platform that harnesses artificial intelligence to deliver personalized education. By adapting to each user's learning style and providing real-time feedback, Sensai AI creates customized learning paths for optimal educational outcomes.

  

---

  

## 🚀 Features

  

### ✨ Adaptive Learning System

- Personalized learning paths

- Real-time progress tracking

- Dynamic difficulty adjustment

- Learning style recognition

  

### 🔬 AI-Powered Analytics

- Performance prediction

- Learning pattern analysis

- Engagement metrics

- Personalized recommendations

  

### 🛠 Interactive Learning Tools

- Virtual tutoring sessions

- Interactive exercises

- Collaborative learning spaces

- Multi-format content support

  

---

  

## 💻 Tech Stack

  

### **Frontend & Backend (Full-Stack with Next.js)**

- Next.js (App Router)

- React.js

- Javascript

- Tailwind CSS

- Prisma ORM

- PostgreSQL

  

## 🏁 Getting Started

  

### Prerequisites

  

Ensure you have the following installed:

  

- [Next.js](https://nextjs.org/) (>= 16.0.0)
 - [Node.js](https://nodejs.org/) (>= 16.0.0)
- [PostgreSQL](https://www.postgresql.org/) (>= 13.0)
- [Python](https://www.python.org/) (>= 3.8)
- npm, yarn, or pnpm

  

### Installation

  

```bash

# Clone the repository
git  clone  https://github.com/SVPraveen1/sensai-ai.git

# Navigate to project directory
cd  sensai-ai

# Install dependencies
pnpm  install

# Start the development server
pnpm  dev

```

  

### Configuration

  

Create a `.env` file in the root directory:

  

```env

NODE_ENV=development

PORT=3000

DATABASE_URL=postgresql://user:password@localhost:5432/sensai

JWT_SECRET=your_jwt_secret

AI_API_KEY=your_ai_api_key

```

  

---

  

## 🏛 Project Structure

  

```

sensai-ai/

├── app/ # Next.js application directory (frontend & API routes)

│ ├── api/ # Backend API routes (Next.js server functions)

│ ├── page.js # Main page component

│ └── ... # Other Next.js specific files

├── components/ # React components

├── data/ # Static data files

├── hooks/ # Custom React hooks

├── lib/ # Library utilities

├── prisma/ # Prisma schema and migrations

├── public/ # Public assets

├── styles/ # CSS and styling files

├── .gitignore # Git ignore file

├── README.md # Project README

├── next.config.mjs # Next.js configuration

├── package.json # Node.js dependencies and scripts

├── pnpm-lock.yaml # pnpm lock file

└── tailwind.config.mjs # Tailwind CSS configuration

```

  

---

  

## 📚 API Documentation

  

Our API follows RESTful principles using Next.js API routes. Full documentation is available at `/docs/api.md`.

  

Example endpoints:

  

```http

GET /api/v1/lessons

POST /api/v1/progress

```

  

---

  

## 🛠 Development

  

```bash

# Run tests

pnpm  test

# Build for production

pnpm  build

```

  

---

  

## 🚢 Deployment

  

Check out the detailed deployment guides for different platforms:

  

- [Deploy to Vercel](https://vercel.com/docs/deployments/overview)


  

---

  

## 🤝 Contributing

  

We welcome contributions! To contribute:

  

1. Fork the repository

2. Create your feature branch (`git checkout -b feature/AmazingFeature`)

3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)

4. Push to the branch (`git push origin feature/AmazingFeature`)

5. Open a Pull Request

  
<!-- ## 🆘 Support

  

- **Documentation:** [Docs](docs/)

- **Issues:** [GitHub Issues](https://github.com/SVPraveen1/sensai-ai/issues)

- **Email:** support@sensai-ai.com

- **Community:** [Join our Discord](https://discord.gg/sensai-ai) -->

  

---

# 🚀 Welth AI Finance

Welth AI is a modern, intelligent personal finance management platform that helps you track, analyze, and optimize your spending with real-time insights. Built with Next.js 14, Prisma, and cutting-edge AI technologies.

![Welth AI Dashboard](public/banner.png)

## 🌟 Features

### Core Features
- **Smart Account Management**
  - Create and manage multiple accounts (Savings & Current)
  - Track account balances and transactions
  - Set default accounts for quick access
  - Real-time balance updates

### Transaction Management
- **Intelligent Transaction Tracking**
  - Record income and expenses with detailed categorization
  - Smart receipt scanner powered by AI
  - Support for recurring transactions (Daily/Weekly/Monthly/Yearly)
  - Multi-currency support
  - Detailed transaction history with advanced filtering

### Analytics and Insights
- **Advanced Analytics**
  - Visual spending patterns with interactive charts
  - Category-wise expense breakdown
  - Custom date range analysis
  - Budget tracking and alerts

### Budgeting Tools
- **Budget Management**
  - Set and track monthly budgets
  - Visual progress indicators
  - Smart notifications for budget limits
  - Category-wise budget allocation

### AI-Powered Features
- **Intelligent Insights**
  - AI-powered receipt scanning and data extraction
  - Smart categorization of transactions
  - Automated financial insights
  - Spending pattern analysis

### User Experience
- **Modern Interface**
  - Responsive design for all devices
  - Dark/Light mode support
  - Real-time updates
  - Intuitive navigation
  - Beautiful UI components

## 🛠 Technology Stack

- **Frontend**
  - Next.js 14 (React)
  - Tailwind CSS
  - Radix UI Components
  - Recharts for data visualization
  - Clerk for authentication
  - React Hook Form for form handling

- **Backend**
  - Next.js Server Actions
  - Prisma ORM
  - PostgreSQL Database
  - Google AI for receipt scanning
  - Inngest for cron jobs and background tasks

- **Third-Party Services**
  - Clerk (Authentication)
  - Resend (Email notifications)
  - Arcjet (Bot protection & Rate limiting)
  - Google AI (Receipt processing)

## ⚙️ Installation

1. **Clone the repository:**
```bash
git clone https://github.com/SVPraveen1/welth-ai.git
cd welth-ai
```

2. **Install dependencies:**
```bash
pnpm install
```

3. **Set up environment variables:**
Create a `.env` file in the root directory with the following variables:

```plaintext
DATABASE_URL=your_postgres_url
NEXTAUTH_SECRET=your_secret_key
NEXT_PUBLIC_API_URL=http://localhost:3000

# Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key

# Email Service
EMAIL_API_KEY=your_resend_api_key

# Bot Protection & Rate Limiting
ARCJET_API_KEY=your_arcjet_api_key

# AI Features
GEMINI_API_KEY=your_gemini_api_key

# Cron Jobs
INNGEST_API_KEY=your_inngest_api_key
```

4. **Initialize the database:**
```bash
pnpm prisma generate
pnpm prisma migrate dev
```

5. **Start the development server:**
```bash
pnpm dev
```

## 📂 Project Structure

```
welth-ai-finance/
├── actions/           # Server actions for data operations
├── app/              # Next.js app router and pages
│   ├── (auth)/      # Authentication routes
│   ├── (main)/      # Main application routes
│   ├── api/         # API endpoints
├── components/       # React components
│   ├── ui/          # Reusable UI components
├── data/            # Static data and configurations
├── emails/          # Email templates
├── hooks/           # Custom React hooks
├── lib/             # Utility functions and configurations
│   ├── inngest/     # Background jobs
│   ├── prisma.js    # Database client
├── prisma/          # Database schema and migrations
└── public/          # Static assets
```

## 🔐 Security Features

- Secure authentication via Clerk
- Rate limiting and bot protection with Arcjet
- Secure database operations with Prisma
- Input validation using Zod
- Protected API routes
- Secure session management

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 💡 Support

For support, email support@welth.ai or create an issue in the repository.