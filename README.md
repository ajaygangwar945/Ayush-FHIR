<img src="frontend/public/project_banner.png"  width="100%" height="200" style="object-fit: cover">

<div align="center">

# 🏥 Ayush FHIR Integration Platform  

### 🌿 Bridging Traditional Ayush Systems with Modern Healthcare Standards

![Status](https://img.shields.io/badge/Status-Active-success?style=flat)
![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=flat)
![FHIR](https://img.shields.io/badge/HL7-FHIR_R4-orange?style=flat)
![Healthcare](https://img.shields.io/badge/Domain-Healthcare-blueviolet?style=flat)

</div>

---

## 🌟 Overview & Mission

The **Ayush FHIR Integration Platform** is a specialized healthcare interoperability solution dedicated to the digital transformation of **Traditional Indian Medicine** (Ayurveda, Yoga, Unani, Siddha, Homoeopathy).

---

## 🎯 Our Mission

To create a seamless, standardized, and secure bridge between ancient medical wisdom and modern clinical data standards (HL7 FHIR), enabling traditional healthcare practitioners to participate in the global digital health ecosystem while maintaining the unique integrity of Ayush terminology.

---

## 🚀 Key Features

| Feature | Description |
|------|-------------|
| 🔍 **Advanced Search** | High-performance search for NAMASTE terms with fuzzy matching and ICD-11 cross-referencing. |
| 🔄 **FHIR Resource Engine** | Auto-generation of HL7 FHIR CodeSystem and ConceptMap resources from CSV datasets. |
| 🌐 **Translation Hub** | Bidirectional terminology mapping between NAMASTE (Traditional) and ICD-11 TM2 (International). |
| 📊 **Dynamic Analytics** | Real-time monitoring of terminology distribution, search trends, and system health. |
| 🛡️ **Admin Suite** | Comprehensive tools for **User Management**, **System Settings**, and **Secure CSV Data Ingestion**. |
| 📱 **Mobile-First UI** | Fully responsive interface optimized for clinical use on tablets, phones, and desktops. |

---

## 🛠️ Tech Stack

### 🎨 Frontend

- **React 18** & **TypeScript**
- **Tailwind CSS** for responsive design
- **Framer Motion** for smooth UI transitions
- **React Query** for efficient data fetching

### ⚙️ Backend

- **Node.js** & **Express**
- **In-Memory DataStore** with persistent CSV synchronization
- **HL7 FHIR R4** Standardization Logic
- **Jest** for automated API testing

---

## 📂 Project Structure

```text
📦 Ayush-FHIR
 ┣ 📂 api                          # Serverless Deployment Bundle (Vercel)
 ┃ ┣ 📂 data                       # Standardized CSV Datasets
 ┃ ┃ ┗ 📜 sample-namaste.csv       # 1,000+ Standardized AYUSH Terminology Records
 ┃ ┗ 📜 index.js                   # Vercel Serverless Function Handler & Cold-Start Loader
 ┣ 📂 frontend                     # React 18 + TypeScript Client Application
 ┃ ┣ 📂 public                     # Static Media, Logos & HTML Shell
 ┃ ┃ ┣ 📜 favicon.svg              # Application Favicon
 ┃ ┃ ┣ 📜 index.html               # SPA Entry Point
 ┃ ┃ ┗ 📜 project_banner.png       # Project Visual Banner
 ┃ ┣ 📂 src                        # Frontend Application Source Code
 ┃ ┃ ┣ 📂 components               # Modular UI Components
 ┃ ┃ ┃ ┣ 📂 Common                 # Shared UI Elements (LoadingSpinner.tsx)
 ┃ ┃ ┃ ┣ 📂 Dashboard              # Widgets (QuickActions, QuickStats, RecentActivity)
 ┃ ┃ ┃ ┗ 📂 Layout                 # Structural Layout (Header, Sidebar, Layout)
 ┃ ┃ ┣ 📂 context                  # State Management Contexts (ThemeContext, ActivityContext)
 ┃ ┃ ┣ 📂 pages                    # 11 Core Functional Workflows
 ┃ ┃ ┃ ┣ 📜 AdminPage.tsx          # System Admin & In-Memory Store Controls
 ┃ ┃ ┃ ┣ 📜 AnalyticsPage.tsx      # Interactive Visual Analytics (Recharts)
 ┃ ┃ ┃ ┣ 📜 AuthPage.tsx           # ABHA OAuth Simulation & Token Management
 ┃ ┃ ┃ ┣ 📜 Dashboard.tsx          # Main Clinical KPI Dashboard
 ┃ ┃ ┃ ┣ 📜 ExportPage.tsx         # Multi-format Data Exporter (JSON/CSV/FHIR)
 ┃ ┃ ┃ ┣ 📜 FHIRPage.tsx           # Interactive HL7 FHIR Resource Explorer
 ┃ ┃ ┃ ┣ 📜 SearchPage.tsx         # Real-time Fuzzy Terminology Search
 ┃ ┃ ┃ ┣ 📜 SystemSettingsPage.tsx # Microservice Endpoints & System Configurations
 ┃ ┃ ┃ ┣ 📜 TranslationPage.tsx    # Bidirectional Terminology Translator (NAMASTE <=> ICD-11)
 ┃ ┃ ┃ ┣ 📜 UploadPage.tsx         # Drag-and-Drop CSV Ingestion & Validation
 ┃ ┃ ┃ ┗ 📜 UserManagementPage.tsx # Role-Based Access Control (Admin, Doctor, Researcher)
 ┃ ┃ ┣ 📂 services                 # API Client Utilities (api.ts - Axios Interceptors)
 ┃ ┃ ┣ 📜 App.tsx                  # Main App Component & Route Lazy Loading
 ┃ ┃ ┣ 📜 index.css                # Global Tailwind CSS Directives & Styles
 ┃ ┃ ┗ 📜 index.tsx                # React DOM Initialization
 ┃ ┣ 📜 package.json               # Frontend Dependencies & Build Scripts
 ┃ ┣ 📜 postcss.config.js          # PostCSS Configuration
 ┃ ┗ 📜 tailwind.config.js         # Tailwind Design System Configuration
 ┣ 📂 src                          # Node.js + Express Core Microservice
 ┃ ┣ 📂 models                     # Data Entity Definitions
 ┃ ┃ ┗ 📜 NamesteTerm.js           # NAMASTE Term Model, Trigram Scoring & Validation
 ┃ ┣ 📂 routes                     # API Route Handlers
 ┃ ┃ ┣ 📜 adminRoutes.js           # /admin Endpoints (Ingest, Statistics, Clear)
 ┃ ┃ ┣ 📜 authRoutes.js            # /auth Endpoints (ABHA OAuth Simulation)
 ┃ ┃ ┣ 📜 fhirRoutes.js            # /fhir Endpoints (CodeSystem & ConceptMap)
 ┃ ┃ ┣ 📜 icdRoutes.js             # /api/icd Endpoints (WHO ICD-11 Search)
 ┃ ┃ ┗ 📜 translationRoutes.js     # /api/translation Endpoints (Bidirectional Translation)
 ┃ ┣ 📂 services                   # Core Business Logic Services
 ┃ ┃ ┣ 📜 auditService.js          # FHIR AuditEvent & Provenance Resource Generators
 ┃ ┃ ┣ 📜 csvParser.js             # High-Speed Streaming CSV Parser & Validator
 ┃ ┃ ┣ 📜 dataStore.js             # In-Memory Store, Trigram Fuzzy Index & Stats Engine
 ┃ ┃ ┣ 📜 fhirService.js           # HL7 FHIR R4 Resource Generator (CodeSystem, ConceptMap)
 ┃ ┃ ┗ 📜 icdService.js            # WHO ICD-11 Client & Token Lifecycle Management
 ┃ ┣ 📂 tests                      # Verification & Integration Test Suite
 ┃ ┃ ┣ 📜 api.test.js              # Core API Endpoint Integration Tests
 ┃ ┃ ┣ 📜 auth.test.js             # ABHA Token & Authorization Tests
 ┃ ┃ ┣ 📜 fhir.test.js             # FHIR Resource Schema Tests
 ┃ ┃ ┣ 📜 icd.test.js              # WHO ICD-11 Service Tests
 ┃ ┃ ┗ 📜 translation.test.js      # Terminology Mapping & Translation Tests
 ┃ ┣ 📂 utils                      # Cross-Platform Utilities
 ┃ ┃ ┗ 📜 paths.js                 # Environment-Aware Data Path Resolver (Local / Serverless)
 ┃ ┗ 📜 server.js                  # Master Express API Server Configuration & Startup
 ┣ 📂 scripts                      # Data Utility Scripts
 ┃ ┗ 📜 generate_namaste_data.js   # Procedural Synthetic AYUSH Dataset Generator
 ┣ 📜 .env                         # Local Environment Variables
 ┣ 📜 .env.example                 # Environment Configuration Template
 ┣ 📜 .gitignore                   # Git Ignore Configuration
 ┣ 📜 package.json                 # Node.js Root Dependencies & Scripts
 ┣ 📜 package-lock.json            # Deterministic Dependency Lock
 ┣ 📜 project_details.txt          # Architectural Specifications & System Documentation
 ┣ 📜 vercel.json                  # Vercel Deployment & URL Rewrite Configuration
 ┣ 📜 verify_api.js                # End-to-End API Health & Search Verification Script
 ┗ 📜 README.md                    # Project Documentation
```

---

## ⚡ Getting Started

### Prerequisites

- **Node.js** (v14 or higher)
- **npm** or **yarn**

### Installation

1. **Clone the repository**

    ```bash
    git clone https://github.com/ajaygangwar945/Ayush-FHIR.git
    cd Ayush-FHIR
    ```

2. **Install Backend Dependencies**

    ```bash
    npm install
    ```

3. **Install Frontend Dependencies**

    ```bash
    cd frontend
    npm install
    ```

### Running the Application

1. **Start the Backend Server**

    ```bash
    # From the root directory
    npm run dev
    ```

2. **Start the Frontend Development Server**

    ```bash
    # From the frontend directory
    npm start
    ```

   The application should now be running at `http://localhost:3000` (frontend) and `http://localhost:5000` (backend).

---

## 🌐 Deployment

This project is deployed using **Vercel** for instant updates and global CDN performance.

[![Vercel Deployment](https://img.shields.io/badge/Vercel-Deployed-black?style=flat&logo=vercel)](https://sih-ayush-fhir.vercel.app/)

1. Updates are pushed to **GitHub**.
2. **Vercel** automatically rebuilds and deploys the changes.
3. The live site is updated instantly 🌍 [Visit Live Site](https://sih-ayush-fhir.vercel.app/)

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

<div align="center">
  <sub>Built with ❤️ by the Ayush FHIR Team</sub>
</div>
