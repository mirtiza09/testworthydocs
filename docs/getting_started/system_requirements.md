---
sidebar_position: 3
---

# System Requirements

This section outlines the hardware and software prerequisites necessary to run TestWorthy effectively. It provides step-by-step instructions to ensure your environment is properly configured for development, testing, and deployment.

## Hardware Requirements

- **Processor:** Minimum of a dual-core CPU (Intel i3 or equivalent). For optimal performance, a quad-core or higher is recommended.
- **Memory:** At least 8 GB RAM. For large test suites or concurrent users, 16 GB or more is advised.
- **Storage:** Minimum of 50 GB free disk space to accommodate source code, dependencies, and data storage.
- **Graphics Card:** Integrated graphics are sufficient; however, a dedicated GPU is recommended if using hardware-accelerated rendering or visualization tools.
- **Network:** Reliable internet connection with at least 10 Mbps bandwidth for downloading dependencies, accessing external integrations, and cloud-based services.

## Software Requirements

### Operating System

- **Development Environment:** Windows 10/11, macOS 10.15+ (Catalina), or Linux distributions (Ubuntu 20.04+, CentOS 8+).
- **Server Deployment:** Compatible with Windows Server 2016/2019, Ubuntu Server 20.04+, or containerized environments like Docker.

### Runtime and Dependencies

- **.NET Core SDK:** Version 6.0 or later for backend services and migration scripts.
- **Node.js:** Version 14.x or later for frontend build processes, including Gulp tasks.
- **Database Server:** SQL Server 2019 or later, or compatible PostgreSQL/MySQL versions if configured.
- **Web Browser:** Modern browsers such as Chrome (latest), Edge, Firefox, or Safari for testing and development.

### Development Tools

- **IDE:** Visual Studio 2022 or later, Visual Studio Code with relevant extensions.
- **Package Managers:** npm (version 6.x+), yarn (optional).
- **Build Tools:** Gulp.js (version 4.x), configured via `gulpfile.js`.
- **Additional Tools:** Git for version control, Docker (optional) for containerized deployment.

## Installation Steps

1. **Verify Hardware Compatibility:** Ensure your machine meets the above hardware specifications.
2. **Install Operating System Updates:** Keep your OS updated for security and compatibility.
3. **Set Up Runtime Environments:**
   - Download and install [.NET 6 SDK](https://dotnet.microsoft.com/download).
   - Download and install [Node.js](https://nodejs.org/).
4. **Configure Database:**
   - Install SQL Server 2019 or later.
   - Create a new database instance for TestWorthy.
   - Apply initial migrations or seed data as per documentation.
5. **Install Development Tools:**
   - Install Visual Studio 2022 with ASP.NET and Web Development workload.
   - Install Git and clone the repository.
   - Run `npm install` in the project directory to fetch dependencies.
6. **Build Frontend Assets:**
   - Run `gulp` commands as specified in `gulpfile.js` to compile styles and scripts.
7. **Configure Environment:**
   - Set environment variables for database connection strings, API keys, and external services.
   - Update configuration files (`appsettings.json`, environment-specific configs).
8. **Run the Application:**
   - Use Visual Studio or CLI (`dotnet run`) to start backend services.
   - Access the application via `http://localhost:5000` or configured URL.
9. **Test Environment:**
   - Verify all components load correctly.
   - Check database connectivity and external integrations.
   - Ensure UI responsiveness and functionality.

## Additional Recommendations

- **Hardware Scaling:** For production, consider load balancers, multiple servers, and scaled database instances.
- **Security:** Implement SSL/TLS, secure database credentials, and adhere to best practices for authentication and authorization.
- **Backup & Recovery:** Regularly backup your database and configuration files.
- **Monitoring:** Use tools like Application Insights, New Relic, or Prometheus for performance monitoring.

By following these system requirements and setup instructions, you will establish a stable environment capable of running TestWorthy efficiently, supporting development, testing, and deployment workflows.