[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

# ACTION-REACTION Platform

An automation platform inspired by IFTTT and Zapier that allows users to create automated workflows by connecting various services through Actions and REActions.

## 🌟 Overview

ACTION-REACTION is a powerful automation platform that enables users to create custom automated workflows (AREAs) by connecting different services. When a specific action occurs in one service, it automatically triggers a reaction in another service.

### Backend (Application Server)

- **FastAPI**: High-performance Python web framework

  - Async support for better performance
  - Automatic API documentation with Swagger UI
  - Built-in data validation
  - WebSocket support for real-time updates
- **MongoDB**: NoSQL Database

  - Flexible document-based structure
  - Excellent scaling capabilities
  - Rich query language
  - Native support for JSON-like documents
- **APScheduler (Advanced Python Scheduler)**

  - Robust job scheduling system
  - Different scheduling mechanisms (interval, cron, one-off)
  - Persistent job storage
  - Job monitoring and management

### Frontend (Web Client)

- **React.js**: JavaScript library for building user interfaces

  - Component-based architecture
  - Virtual DOM for optimal performance
  - Rich ecosystem of libraries
  - Reusable UI components
- **Tailwind CSS**: Utility-first CSS framework

  - Highly customizable
  - Responsive design out of the box
  - Low-level utility classes
  - Efficient build system

### Mobile Client

- **React Native**: Cross-platform mobile development
  - Native performance
  - Code sharing with web client
  - Hot reloading for faster development
  - Access to native APIs

### Architecture Components

- **Application Server**: Core backend handling business logic (Port 8080)
- **Web Client**: Browser-based interface (Port 8081)
- **Mobile Client**: Android application for on-the-go access

# Diagram

[View on Eraser![](https://app.eraser.io/workspace/Go9WvtHyDxLdwLXyLZBN/preview?elements=TCYOQd8F3b3bPO73ajb8tw&type=embed)](https://app.eraser.io/workspace/Go9WvtHyDxLdwLXyLZBN?elements=TCYOQd8F3b3bPO73ajb8tw)

## 🚀 Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

1. Clone the repository:

```bash
git clone https://github.com/EpitechPromo2027/B-DEV-500-COT-5-2-area-shalom.dosseh.git
cd B-DEV-500-COT-5-2-area-shalom.dosseh
```

2. Build the containers:

```bash
docker compose build
```

3. Start the services:

```bash
docker compose up
```

### Accessing the Platform

- Web Interface: http://localhost:8081
- Mobile APK: http://localhost:8081/client.apk
- API Documentation: http://localhost:8080/about.json

## 🔧 Core Features

### Web Client

![FrontEnd](assets/front_explore.jpg)

- User connect to different service (eg. Google Mail, Google Task, Telegram, etc...)

![Create](assets/front_create.jpg)

- Users can create a workflow by selecting an action or reaction (eg. If new task is added then send a mail)

## 📡 API Reference

![API_REF](https://github.com/EpitechPromo2027/B-DEV-500-COT-5-2-area-shalom.dosseh/blob/feature/server/assets/api_ref.gif))

### Base URLs

- API Url: `http://127.0.0.1:8080`
- Web Client Url: `http://127.0.0.1:8081`

### API Documentation

Our API provides two different styles of documentation to suit varying needs:

1. **Interactive Swagger UI Docs**Access the interactive API documentation powered by Swagger UI. This allows you to:

   - View all available API endpoints.
   - See request and response examples.
   - Test the API directly within the browser.

   URL: [http://127.0.0.1:8080/docs](http://127.0.0.1:8080/docs)
2. **ReDoc Static Documentation**Access a clean and user-friendly static view of the API documentation powered by ReDoc. This is ideal for:

   - Developers who want a neatly structured, scrollable API reference.
   - Users who prefer a read-only format without the ability to test requests.

   URL: [http://127.0.0.1:8080/redoc](http://127.0.0.1:8080/redoc)

---

## 🛠️ Technical Architecture

### Docker Services

The platform uses Docker Compose with three main services:

1. **server**: Application server (Port 8080)

   - Handles business logic
   - Exposes REST API
   - Manages service integrations
2. **client_web**: Web interface (Port 8081)

   - User interface
   - Request forwarding to server
   - Mobile client APK distribution
3. **client_mobile**: Mobile application builder

   - Builds Android application
   - Shares volume with client_web
   - Configurable server connection

## 🔒 Security

- OAuth2 implementation for user authentication
- Secure API endpoints
- Data encryption
- Access token management

## 💡 Development Guidelines

- Follow REST API best practices
- Implement proper error handling
- Write comprehensive unit tests
- Document new features and APIs
- Follow accessibility guidelines
- Maintain separation of concerns between clients and server

## 👥 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.
