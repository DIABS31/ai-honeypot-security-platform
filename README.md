# 🛡️ AI Honeypot Security Platform

> **Enterprise-Grade SOC Platform** combining honeypots, real-time threat detection, and machine learning for advanced cybersecurity defense.

![License](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/python-3.12+-blue)
![React](https://img.shields.io/badge/react-18+-blue)
![Docker](https://img.shields.io/badge/docker-latest-blue)
![Status](https://img.shields.io/badge/status-production-green)

## 📋 Quick Links

- [📖 Installation Guide](docs/INSTALLATION.md)
- [🔌 API Documentation](docs/API.md)
- [🚀 Deployment Guide](docs/DEPLOYMENT.md)
- [👤 User Guide](docs/USER_GUIDE.md)
- [⚙️ Admin Guide](docs/ADMIN_GUIDE.md)
- [🛡️ Security Guide](docs/SECURITY.md)

## 🎯 Overview

The **AI Honeypot Security Platform** is a sophisticated cybersecurity defense system designed for Security Operations Centers (SOC) and enterprise blue teams. It deploys multiple honeypots to attract and analyze cyber threats while leveraging machine learning to automatically classify and respond to attacks in real-time.

### Perfect For:
- 🏢 Enterprise Security Operations
- 🎓 Cybersecurity Education & Research
- 🔍 Threat Intelligence Collection
- 📊 Security Posture Analysis
- 🛡️ Advanced Persistent Threat (APT) Detection

## ✨ Key Features

### 🚀 Honeypot Deployment
- **Cowrie**: SSH/Telnet honeypot with realistic Linux simulation
- **Dionaea**: Malware honeypot for binary threat capture

### 🤖 AI & Machine Learning
- ✅ Real-Time Threat Classification
- ✅ Anomaly Detection (Isolation Forest)
- ✅ Ensemble Models (Random Forest + XGBoost)
- ✅ SHAP Explainability
- ✅ Predictive Scoring (0-100 scale)

### 📊 Advanced Analytics
- ✅ Real-Time Dashboard with WebSocket
- ✅ Threat Timeline Visualization
- ✅ Global Geographic Heatmap
- ✅ Behavioral Pattern Recognition
- ✅ Predictive Risk Assessment

### 🎨 Modern SOC Interface
- ✅ Glassmorphism UI Design
- ✅ Neon Cyber Aesthetics
- ✅ Real-time Data Updates
- ✅ Fully Responsive Layout
- ✅ Dark Theme for SOC Environments

### ⚙️ Enterprise Features
- ✅ JWT Authentication with RBAC
- ✅ Multi-Tenant Support (Admin, Analyst, Read-Only)
- ✅ Alert Management System
- ✅ Report Generation (CSV, Excel, PDF)
- ✅ Comprehensive Audit Logging
- ✅ Scalable Docker Architecture

## 🏗️ Architecture

```
┌────────────────────────────────────────┐
│    React Frontend (Port 3000/5173)     │
│   Modern SOC Dashboard & Real-time UI   │
└──────────────────┬─────────────────────┘
                   │ WebSocket
┌──────────────────▼─────────────────────┐
│     FastAPI Backend (Port 8000)        │
│  ┌──────────────┐ ┌───────────────┐   │
│  │ REST API     │ │ WebSocket     │   │
│  │ Controllers  │ │ Manager       │   │
│  └──────────────┘ └───────────────┘   │
│  ┌──────────────┐ ┌───────────────┐   │
│  │ ML Pipeline  │ │ Auth & RBAC   │   │
│  │ (Detection)  │ │ System        │   │
│  └──────────────┘ └───────────────┘   │
└──┬────────┬────────┬─────────────────┘
   │        │        │
   │      Cache    Queue
  DB      Redis   RabbitMQ
   │
   └─ Honeypots Network
      ├─ Cowrie (SSH/Telnet)
      └─ Dionaea (Malware)
```

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Git
- 8GB RAM minimum
- 10GB disk space

### One-Command Deployment

```bash
# Clone repository
git clone https://github.com/DIABS31/ai-honeypot-security-platform.git
cd ai-honeypot-security-platform

# Start all services
docker-compose up -d

# Wait for services to be ready (2-3 minutes)
sleep 180

# Access the platform
echo "Frontend: http://localhost:3000"
echo "API Docs: http://localhost:8000/docs"
echo "Admin: http://localhost:8000/admin"
```

### Default Credentials

```
Username: admin
Password: admin123
```

⚠️ **Change immediately in production!**

## 📦 Installation

For detailed installation instructions, see [INSTALLATION.md](docs/INSTALLATION.md)

### Quick Setup (Manual)

```bash
# Backend
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
alembic upgrade head
uvicorn main:app --reload

# Frontend (new terminal)
cd frontend
npm install
npm run dev
```

## 📚 Documentation

| Document | Purpose |
|----------|----------|
| [INSTALLATION.md](docs/INSTALLATION.md) | Detailed setup guide |
| [API.md](docs/API.md) | Complete API reference |
| [DEPLOYMENT.md](docs/DEPLOYMENT.md) | Production deployment |
| [USER_GUIDE.md](docs/USER_GUIDE.md) | End-user documentation |
| [ADMIN_GUIDE.md](docs/ADMIN_GUIDE.md) | Administrator guide |
| [SECURITY.md](docs/SECURITY.md) | Security hardening |
| [ML_MODELS.md](docs/ML_MODELS.md) | ML pipeline details |
| [TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Common issues |

## 💻 Technology Stack

### Backend
| Component | Technology | Version |
|-----------|-----------|----------|
| Language | Python | 3.12+ |
| Framework | FastAPI | 0.104+ |
| Database | PostgreSQL | 15+ |
| Cache | Redis | 7+ |
| ORM | SQLAlchemy | 2.0+ |
| Auth | JWT | - |

### Frontend
| Component | Technology | Version |
|-----------|-----------|----------|
| Framework | React | 18+ |
| Language | TypeScript | 5+ |
| Bundler | Vite | 5+ |
| Styling | TailwindCSS | 3+ |
| UI Library | Shadcn/UI | Latest |
| Charts | Recharts | 2.10+ |
| Icons | Lucide | Latest |
| Animation | Framer Motion | 10+ |

### Machine Learning
| Component | Technology | Purpose |
|-----------|-----------|----------|
| Classification | Scikit-Learn | Threat detection |
| Boosting | XGBoost | Enhanced accuracy |
| Anomaly | Isolation Forest | Unknown threats |
| Explainability | SHAP | Model transparency |
| Data | Pandas | Feature engineering |

### DevOps
| Component | Technology | Purpose |
|-----------|-----------|----------|
| Containerization | Docker | Service isolation |
| Orchestration | Docker Compose | Service management |
| Web Server | Nginx | Reverse proxy |
| Honeypots | Cowrie, Dionaea | Threat capture |

## 📊 Dashboard Features

### KPI Cards
- 📈 Total Attacks
- 🎯 Attacks Today
- 🔴 Critical Threats
- 🌍 Unique IPs
- 🗺️ Countries Detected
- 🦠 Malware Captured

Each card includes:
- ✨ Smooth animations
- 📊 Trend percentage
- 🎨 Glassmorphism design
- 🔄 Real-time updates

### Visualizations
- 📈 Attacks by Hour
- 📅 Attacks by Day
- 🔝 Top Attacking IPs
- 🎯 Top Targeted Ports
- 🛡️ Attack Types Distribution
- 📡 Protocol Usage
- ⚠️ AI Risk Score Trend

### Threat Intelligence
- 🔍 Real-time threat feed
- 🌐 Geographic analysis
- 📊 Behavioral patterns
- 🤖 AI classification
- 🎯 Confidence scores

## 🤖 AI & Machine Learning

### Features Used
```python
features = [
    'attempt_count',      # Number of login attempts
    'frequency',          # Attack frequency
    'country_code',       # Origin country
    'target_port',        # Target port
    'honeypot_type',      # Honeypot engaged
    'user_agent',         # Client user agent
    'command_count',      # Commands executed
    'session_duration',   # Session length
]
```

### Threat Classification
- 🔐 Brute Force
- 🔑 Credential Stuffing
- 🔎 Reconnaissance
- 🦠 Malware
- 🤖 Botnet
- 🔌 Port Scan
- ❓ Unknown

### Model Performance
- Accuracy: ~95%
- Precision: ~93%
- Recall: ~94%
- F1-Score: ~0.935

## 🔒 Security

### Authentication
- ✅ JWT tokens with refresh rotation
- ✅ Bcrypt password hashing
- ✅ Role-based access control (RBAC)
- ✅ API rate limiting
- ✅ CORS protection

### Data Protection
- ✅ PostgreSQL encrypted connections
- ✅ Redis TLS support
- ✅ SQL injection prevention (ORM)
- ✅ XSS protection
- ✅ CSRF tokens

### Compliance
- ✅ GDPR ready
- ✅ Audit logging
- ✅ Data retention policies
- ✅ User consent management

## 📈 Performance

### Benchmarks
- Threat Detection: < 100ms
- API Response: < 200ms
- WebSocket Update: < 50ms
- Dashboard Load: < 2s
- Throughput: 10,000+ attacks/hour

### Optimization
- Query caching with Redis
- Database indexing
- Connection pooling
- Frontend code splitting
- Asset compression

## 🧪 Testing

### Backend Tests
```bash
cd backend
pytest tests/ -v
pytest tests/ --cov=app --cov-report=html
```

### Frontend Tests
```bash
cd frontend
npm run test
npm run test:coverage
```

## 📁 Project Structure

```
ai-honeypot-security-platform/
├── backend/                    # FastAPI backend
│   ├── app/
│   │   ├── main.py            # Application entry
│   │   ├── config.py          # Configuration
│   │   ├── models/            # Database models
│   │   ├── schemas/           # Pydantic schemas
│   │   ├── api/               # API routes
│   │   ├── services/          # Business logic
│   │   ├── ml/                # ML pipeline
│   │   ├── websockets/        # WebSocket handlers
│   │   └── security/          # Auth & security
│   ├── migrations/            # Database migrations
│   ├── tests/                 # Unit tests
│   ├── requirements.txt       # Dependencies
│   └── .env.example           # Environment template
│
├── frontend/                   # React frontend
│   ├── src/
│   │   ├── components/        # React components
│   │   ├── pages/             # Page components
│   │   ├── hooks/             # Custom hooks
│   │   ├── services/          # API services
│   │   ├── store/             # State management
│   │   ├── styles/            # Global styles
│   │   ├── utils/             # Utilities
│   │   └── App.tsx            # Main app
│   ├── public/                # Static assets
│   └── package.json
│
├── honeypots/                 # Honeypot configs
│   ├── cowrie/                # Cowrie config
│   └── dionaea/               # Dionaea config
│
├── docker-compose.yml         # Development compose
├── docker-compose.prod.yml    # Production compose
├── nginx/                     # Nginx config
├── docs/                      # Documentation
├── scripts/                   # Utility scripts
└── .gitignore
```

## 🚀 Deployment

### Docker Deployment

```bash
# Development
docker-compose up -d

# Production
docker-compose -f docker-compose.prod.yml up -d

# Scale backend
docker-compose -f docker-compose.prod.yml up -d --scale backend=3

# View logs
docker-compose logs -f backend
```

### Cloud Deployment
- See [AWS_DEPLOYMENT.md](docs/deployment/AWS.md)
- See [AZURE_DEPLOYMENT.md](docs/deployment/AZURE.md)
- See [GCP_DEPLOYMENT.md](docs/deployment/GCP.md)

## 🤝 Contributing

### Development Setup
```bash
git clone <repo>
cd ai-honeypot-security-platform
python -m venv venv
source venv/bin/activate
pip install -r backend/requirements-dev.txt
npm install --prefix frontend
```

### Code Style
```bash
# Backend
black backend/
pylint backend/
mypy backend/

# Frontend
npm run lint
npm run format
```

### Pull Request Process
1. Create feature branch: `git checkout -b feature/amazing-feature`
2. Commit changes: `git commit -m "Add amazing feature"`
3. Push to branch: `git push origin feature/amazing-feature`
4. Open Pull Request

## 📞 Support

### Documentation
- 📖 Full docs in `docs/` directory
- 🤔 FAQ: [docs/FAQ.md](docs/FAQ.md)
- 🐛 Known Issues: [docs/KNOWN_ISSUES.md](docs/KNOWN_ISSUES.md)

### Getting Help
- 💬 Discussions: GitHub Discussions
- 🐛 Issues: GitHub Issues
- 📧 Email: support@yourdomain.com

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## ⚖️ Legal Disclaimer

This platform is designed for **authorized security testing only**. Users are responsible for:
- Obtaining proper authorization before deploying honeypots
- Complying with local cybersecurity laws
- Protecting captured threat intelligence
- Following responsible disclosure practices

## 🌟 Acknowledgments

- [Cowrie Project](https://github.com/cowrie/cowrie)
- [Dionaea Project](https://github.com/DinoTools/dionaea)
- [OWASP](https://owasp.org/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [React](https://react.dev/)
- Security research community

---

**Made with ❤️ by Cybersecurity Professionals**

*Last Updated: 2026-05-31*
