#  Wildlife Rescue Centre

An intelligent **Wildlife Rescue & Care Management System** built with **Spring Boot** and **Vanilla Javascript**.  
It automates animal monitoring and rescue management using **AI-powered image analysis**, helping volunteers and rescue teams efficiently track animal health, rescue cases, and recovery progress.

---

##  Features
-  Manage animal records with health and class details  
-  Track rescue cases and critical incidents  
-  AI-based animal image analysis for monitoring  
-  Volunteer and rescue team coordination  
-  Dashboard overview with key stats

---

## Overview
WildGuard is a comprehensive real-time coordination platform designed specifically for wildlife rescue operations. Built with Spring Boot and Vanilla JavaScript, it bridges the gap between field responders, veterinarians, and rescue coordinators through intelligent automation and seamless communication.
The platform combines traditional rescue management workflows with cutting-edge AI-powered capabilities including automated species identification, medical report summarization, and predictive hotspot analysis. Whether you're tracking an injured eagle in the field or coordinating a multi-team rescue operation, WildGuard ensures critical information flows instantly to everyone who needs it.
Why WildGuard?

⚡ Real-Time Coordination - WebSocket-powered live updates eliminate information delays
🤖 AI-Enhanced Decision Making - Reduce cognitive load with intelligent assistance
🗺️ Geospatial Awareness - Map-based incident tracking and hotspot predictions
📱 Field-Ready Design - Responsive interface that works on mobile devices in remote areas
🔒 Secure & Compliant - Built with privacy and data protection in mind



## 🖥️ Screenshots

### Dashboard Overview
<img width="1913" height="947" alt="image" src="https://github.com/user-attachments/assets/6bcaa5e2-5018-45ed-abf3-beb3a288e650" />


### Animal Details
<img width="1896" height="967" alt="image" src="https://github.com/user-attachments/assets/a9199a4e-6412-4e41-ad7b-59e7ee1a7069" />


---

##  Tech Stack
**Frontend:** Vanila Javascript, HTML, CSS
**Backend:** Spring Boot, Java  
**Database:** MySQL  
**AI Integration:** External Model API


Quick Start with Docker
```
# Clone the repository
git clone https://github.com/yourusername/wildguard.git
cd wildguard

# Start all services with Docker Compose
docker-compose up -d

# Access the application
open http://localhost:8080
```

Manual Installation
1. Database Setup
```
# Create database
mysql -u root -p
CREATE DATABASE wildguard_db;
CREATE USER 'wildguard_user'@'localhost' IDENTIFIED BY 'your_secure_password';
GRANT ALL PRIVILEGES ON wildguard_db.* TO 'wildguard_user'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```

2. Backend Setup
```
# Navigate to backend directory
cd backend

# Configure application.properties
cp src/main/resources/application.properties.example src/main/resources/application.properties
# Edit application.properties with your database credentials and API keys

# Build the project
mvn clean install

# Run the application
mvn spring-boot:run
```

3. Frontend Setup
```
# Navigate to frontend directory
cd frontend

# If using npm for dependencies
npm install

# Start development server (if applicable)
npm start

# Or simply open index.html in a browser for static serving
```

4. Environment Variables
Create a .env file in the backend root:
```
# Database Configuration
DB_HOST=localhost
DB_PORT=3306
DB_NAME=wildguard_db
DB_USERNAME=wildguard_user
DB_PASSWORD=your_secure_password

# JWT Configuration
JWT_SECRET=your_jwt_secret_key_min_256_bits
JWT_EXPIRATION=86400000

# AI Service API Keys
OPENAI_API_KEY=your_openai_key
GOOGLE_CLOUD_VISION_KEY=your_google_cloud_key

# File Upload Configuration
MAX_FILE_SIZE=10MB
UPLOAD_DIR=./uploads

# WebSocket Configuration
WEBSOCKET_MESSAGE_SIZE_LIMIT=65536

# Email Configuration (optional)
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_app_password
```


## Documentation
API Documentation
The REST API is fully documented with OpenAPI/Swagger. Once the application is running, visit:
```
http://localhost:8080/swagger-ui.html
```

Key Endpoints
Authentication
```
POST /api/auth/login
POST /api/auth/register
POST /api/auth/refresh-token
```


🤝 Contributing
We welcome contributions from the community! Whether you're fixing bugs, adding features, or improving documentation, your help makes WildGuard better.
Getting Started

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add some amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

Development Guidelines

Follow existing code style and conventions
Write unit tests for new features
Update documentation as needed
Keep commits atomic and descriptive
Ensure all tests pass before submitting PR

Code Style

Java: Follow Google Java Style Guide
JavaScript: ESLint configuration provided
SQL: Uppercase keywords, snake_case for identifiers


🐛 Bug Reports & Feature Requests
Found a bug or have an idea for improvement?

Bug Reports: Open an issue
Feature Requests: Suggest a feature

Please provide as much detail as possible including:

Steps to reproduce (for bugs)
Expected vs actual behavior
Environment details (OS, browser, versions)
Screenshots if applicable


📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments

Wildlife Rescue Organizations who provided valuable feedback during development
Open Source Community for the amazing tools and libraries
Contributors who dedicate their time to improving this platform
Conservation Technologists pioneering the field of AI for wildlife


📞 Contact & Support

Project Maintainer: Thirukaalathessvarar S (eswar2005s@gmail.com)
Documentation: Wiki
