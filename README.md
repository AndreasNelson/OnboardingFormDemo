# Full-Stack Client Onboarding Technical Demonstration

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Express](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)](https://expressjs.com/)
[![Turso](https://img.shields.io/badge/Turso-000000?style=flat&logo=sqlite&logoColor=white)](https://turso.tech/)
[![Jest](https://img.shields.io/badge/Jest-C21325?style=flat&logo=jest&logoColor=white)](https://jestjs.io/)

A high-performance, production-ready implementation of a multi-step client onboarding workflow. This project serves as a technical showcase for modern full-stack development patterns, focusing on **UX fluidity**, **data security**, and **architectural scalability**.

---

## 🛠️ Core Engineering Highlights

### ⚡ Optimized Performance & UX
- **Edge-Ready Data Layer**: Implemented **LibSQL (Turso)** for ultra-low latency data access, utilizing SQLite at the edge.
- **Asynchronous Synchronization**: Engineered a non-blocking background sync process for database operations, ensuring zero impact on user interaction latency.
- **Fluid Motion Orchestration**: Leveraged **Framer Motion** in conjunction with **Mantine v7** to create a tactile, responsive UI with immediate state feedback.
- **State Persistence**: Developed a UUID-based session tracking system allowing for seamless resumption of onboarding progress across multiple sessions and devices.

### 🛡️ Security Architecture
- **Multi-Layer Data Masking**: Engineered a proactive redaction system at the model layer to mask sensitive payment information before persistence, adhering to industry security standards (PCI-DSS).
- **Hardened HTTP Layer**: Integrated **Helmet.js** for robust security headers and implemented strict **CORS** policies to mitigate cross-origin vulnerabilities.
- **Context-Aware Validation**: Implemented dual-layer input validation and sanitization on both the React frontend and Express backend.

### 🧪 Engineering Excellence
- **Comprehensive Test Coverage**: Achieved and maintained **100% line coverage** across the entire stack using **Jest** and **React Testing Library**.
- **Service-Oriented Design**: Decoupled core business logic into specialized services (CRM synchronization, notification engines) to ensure modularity and ease of extension.
- **Full-Stack Type Safety**: Enforced end-to-end TypeScript to guarantee structural integrity and significantly reduce runtime errors.

---

## 🏗️ Technical Stack

### Frontend Architecture
- **React 18**: Utilizing modern hooks and functional components.
- **Mantine v7**: Core component library for consistent, accessible UI.
- **Framer Motion**: Advanced animation orchestration.
- **React Router 6**: Navigation with future-proof configuration.

### Backend Infrastructure
- **Node.js + Express**: RESTful API architecture.
- **LibSQL**: High-performance SQLite implementation for distributed environments.
- **Security Middleware**: Helmet.js, CORS, and custom masking filters.

---

## 🏛️ Project Structure

```text
├── frontend/             # React SPA (Vite)
│   ├── src/components/   # Presentation and container components
│   ├── src/context/      # Global state management via Context API
│   └── src/hooks/        # Encapsulated business logic
└── backend/              # Express API
    ├── src/models/       # Data persistence and masking logic
    ├── src/services/     # Decoupled business services (CRM, Notify)
    └── src/routes/       # Endpoint definitions and route handlers
```

---

## 🚀 Execution & Deployment

### Local Development

1. **Environment Setup**:
   ```bash
   git clone <repository-url>
   cd OnboardingFormDemo
   cd backend && npm install
   cd ../frontend && npm install
   ```

2. **Running Services**:
   - **Backend**: `cd backend && npm run dev` (Default: Port 5000)
   - **Frontend**: `cd frontend && npm run dev` (Default: Port 3000)

### Testing Suite

```bash
# Execute full test suite
cd backend && npm test
cd frontend && npm test

# Generate coverage reports
npm run test:coverage
```

---

## 📝 Technical Roadmap
- [ ] Transition from mocked CRM endpoints to production API integrations.
- [ ] Implement backend-driven dynamic step injection.
- [ ] Integrate server-side PDF generation for service agreements.

---

## 📄 License
Distributed under the MIT License.
