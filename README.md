# GRC-Platform---Information-Security-Governance-Risk-and-Compliance
A Docker-based platform for automating Information Security GRC processes with RBAC, dashboards, audit finding management, and risk assessment capabilities.

## Features

- **Role-Based Access Control (RBAC)**: Secure access with different permission levels
- **Audit Finding Management**: Track, review, and manage audit findings with comments and target dates
- **Risk Management**: Comprehensive risk assessment workflows
- **Compliance Tracking**: Monitor compliance with ISO 27001, SAMA Frameworks, and KSA NCA guidelines
- **Dashboard**: Visual overview of key metrics and pending items
- **Audit Trail**: Track all changes and comments for accountability
- **Comment System**: Allow auditees to incorporate their comments
- **Notification System**: Keep track of deadlines and updates

## Technology Stack

- **Frontend**: React.js with Bootstrap
- **Backend**: FastAPI (Python)
- **Database**: PostgreSQL
- **Infrastructure**: Docker & Docker Compose
- **Authentication**: JWT-based authentication
- **Reverse Proxy**: Nginx

## Prerequisites

- Docker
- Docker Compose

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd grc-platform
   ```

2. Navigate to the docker directory:
   ```bash
   cd docker
   ```

3. Start the services:
   ```bash
   docker-compose up -d
   ```

4. The application will be available at:
   - Frontend: http://localhost
   - API Documentation: http://localhost/docs

## Services

- **Frontend**: React application (port 3000)
- **Backend**: FastAPI application (port 8000)
- **Database**: PostgreSQL (port 5432)
- **Nginx**: Reverse proxy (port 80)

## Project Structure

```
grc-platform/
├── backend/          # FastAPI backend application
│   ├── main.py       # Main application file
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/         # React frontend application
│   ├── src/
│   │   ├── components/
│   │   │   ├── Login.js
│   │   │   ├── Dashboard.js
│   │   │   ├── AuditFindings.js
│   │   │   ├── RiskAssessment.js
│   │   │   └── Compliance.js
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── Dockerfile
├── docker/           # Docker configurations
│   ├── docker-compose.yml
│   └── nginx.conf
└── README.md
```

## API Endpoints

- `POST /token` - Authentication
- `POST /users/` - Create user
- `GET /users/me/` - Get current user
- `POST /audit_findings/` - Create audit finding
- `GET /audit_findings/` - List audit findings
- `POST /comments/` - Add comment to finding

## Development

To develop locally without Docker:

### Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend
```bash
cd frontend
npm install
npm start
```

## Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Role-based access control
- Audit trail for all changes
- Secure API with validation

## Compliance Frameworks Supported

- ISO 27001
- SAMA Frameworks (Saudi Arabia)
- KSA NCA Guidelines (Saudi Arabia)

## Future Enhancements

- Integration with vulnerability scanners
- Automated compliance reporting
- Advanced risk scoring algorithms
- Multi-tenancy support
- Mobile-responsive design
- Advanced notification system
- Integration with ticketing systems
- Evidence repository for compliance
- Policy management workflows

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a pull request

## License

This project is licensed under the MIT License.
