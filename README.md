# 📄 ResuMate

<div align="center">

![ResuMate](https://img.shields.io/badge/ResuMate-AI%20Resume%20Analyzer-8e98ff?style=for-the-badge)
![React](https://img.shields.io/badge/React-19.2.3-61DAFB?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9.2-3178C6?style=flat-square&logo=typescript)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.1.13-06B6D4?style=flat-square&logo=tailwindcss)
![React Router](https://img.shields.io/badge/React%20Router-7.12.0-CA4245?style=flat-square&logo=reactrouter)

**Smart feedback for your dream job!** 🚀

[Features](#-features) • [Tech Stack](#-tech-stack) • [Getting Started](#-getting-started) • [Screenshots](#-screenshots) • [Deployment](#-deployment)

</div>

---

## 🌟 Overview

**ResuMate** is a full-stack AI-powered resume analyzer that helps job seekers optimize their resumes for Applicant Tracking Systems (ATS) and improve their chances of landing interviews. Upload your resume, provide job details, and receive comprehensive, actionable feedback powered by AI.

## ✨ Features

### 🤖 AI-Powered Resume Analysis

- **ATS Compatibility Score** - Get instant feedback on how well your resume performs with Applicant Tracking Systems
- **Overall Resume Rating** - Receive a comprehensive score (out of 100) based on multiple factors
- **Detailed Feedback Categories**:
  - 📝 **Content Analysis** - Evaluate the quality and relevance of your resume content
  - 🎨 **Tone & Style** - Assess professional language and presentation
  - 📐 **Structure Review** - Check resume layout and organization
  - 💼 **Skills Matching** - Measure alignment with job requirements

### 🎯 Job-Specific Analysis

- Input **company name**, **job title**, and **job description** for tailored feedback
- Receive recommendations customized to your target position
- AI considers your specific job requirements when analyzing

### 📊 Resume Dashboard

- Track all your uploaded resumes in one place
- View historical analysis results
- Compare scores across different resume versions
- Visual score gauges and progress indicators

### 🔐 Secure Authentication

- User authentication via Puter.js
- Personal resume storage with cloud-based file system
- Key-value store for resume metadata

## 🛠 Tech Stack

### Frontend

| Technology         | Purpose                             |
| ------------------ | ----------------------------------- |
| **React 19**       | UI library with latest features     |
| **React Router 7** | Full-stack routing with SSR support |
| **TypeScript**     | Type-safe development               |
| **TailwindCSS 4**  | Utility-first styling               |
| **Zustand**        | Lightweight state management        |

### Backend & Services

| Technology           | Purpose                                    |
| -------------------- | ------------------------------------------ |
| **Puter.js**         | Authentication, AI, File Storage, KV Store |
| **React Router SSR** | Server-side rendering                      |
| **PDF.js**           | PDF to image conversion                    |

### Development Tools

| Tool       | Purpose                      |
| ---------- | ---------------------------- |
| **Vite 7** | Fast build tool & dev server |
| **Docker** | Containerized deployment     |

## 📁 Project Structure

```
ResumeAnalyzer/
├── app/
│   ├── components/          # Reusable UI components
│   │   ├── ATS.tsx          # ATS score display
│   │   ├── Accordion.tsx    # Expandable feedback sections
│   │   ├── Details.tsx      # Detailed feedback view
│   │   ├── FileUploader.tsx # Drag & drop file upload
│   │   ├── Navbar.tsx       # Navigation bar
│   │   ├── ResumeCard.tsx   # Resume preview card
│   │   ├── ScoreBadge.tsx   # Score indicator badges
│   │   ├── ScoreCircle.tsx  # Circular score display
│   │   ├── ScoreGauge.tsx   # Visual score gauge
│   │   └── Summary.tsx      # Feedback summary
│   ├── lib/                 # Utility libraries
│   │   ├── pdf2img.ts       # PDF to image converter
│   │   ├── puter.ts         # Puter.js integration & state
│   │   └── utils.ts         # Helper utilities
│   ├── routes/              # Application routes
│   │   ├── Auth.tsx         # Authentication page
│   │   ├── home.tsx         # Dashboard/home page
│   │   ├── Resume.tsx       # Resume detail view
│   │   ├── Upload.tsx       # Resume upload page
│   │   └── Wipe.tsx         # Data management
│   ├── app.css              # Global styles & theme
│   ├── root.tsx             # App root component
│   └── routes.ts            # Route configuration
├── constants/               # App constants & AI prompts
├── public/
│   ├── icons/               # UI icons (SVG)
│   └── images/              # Images & backgrounds
├── types/                   # TypeScript type definitions
├── Dockerfile               # Docker configuration
├── package.json             # Dependencies & scripts
├── tsconfig.json            # TypeScript configuration
└── vite.config.ts           # Vite configuration
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** 20.x or higher
- **npm** or **pnpm**

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Anuragx456/resume-analyzer.git
   cd resume-analyzer
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start development server**

   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:5173
   ```

### Available Scripts

| Command             | Description                       |
| ------------------- | --------------------------------- |
| `npm run dev`       | Start development server with HMR |
| `npm run build`     | Create production build           |
| `npm run start`     | Run production server             |
| `npm run typecheck` | Run TypeScript type checking      |

## 📸 Screenshots

### 🏠 Home Dashboard

Track all your resume submissions and view AI-powered feedback scores at a glance.

### 📤 Upload Page

- Drag & drop PDF resume upload
- Enter job details (company, title, description)
- Real-time processing status with animated indicators

### 📊 Resume Analysis

- Side-by-side resume preview with feedback
- ATS compatibility score with improvement tips
- Detailed breakdowns for content, style, structure, and skills
- Actionable suggestions marked as ✅ strengths or ⚠️ areas to improve

## 🐳 Deployment

### Docker Deployment

1. **Build the Docker image**

   ```bash
   docker build -t resumate .
   ```

2. **Run the container**

   ```bash
   docker run -p 3000:3000 resumate
   ```

3. **Access the application**
   ```
   http://localhost:3000
   ```

### Supported Platforms

The containerized application can be deployed to:

- ☁️ **AWS ECS**
- ☁️ **Google Cloud Run**
- ☁️ **Azure Container Apps**
- 🌊 **Digital Ocean App Platform**
- 🪁 **Fly.io**
- 🚂 **Railway**

### Manual Deployment

For manual deployment, ensure you deploy the output of `npm run build`:

```
├── package.json
├── package-lock.json
├── build/
│   ├── client/    # Static assets
│   └── server/    # Server-side code
```

## 🔧 Configuration

### AI Response Format

ResuMate uses a structured feedback format for AI analysis:

```typescript
interface Feedback {
  overallScore: number; // Overall score (0-100)
  ATS: {
    score: number; // ATS compatibility score
    tips: TipItem[]; // ATS improvement tips
  };
  toneAndStyle: ScoreSection; // Writing style feedback
  content: ScoreSection; // Content quality feedback
  structure: ScoreSection; // Layout/structure feedback
  skills: ScoreSection; // Skills alignment feedback
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Built with ❤️ using React Router & Puter.js**

⭐ Star this repository if you found it helpful!

</div>
