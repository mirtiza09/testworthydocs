---
sidebar_position: 4
---

# Installation Guide

This section provides step-by-step instructions for deploying TestWorthy in both cloud and on-premises environments. Follow the appropriate instructions based on your deployment preference.

## Cloud Deployment

To set up TestWorthy in the cloud, follow these steps:

1. **Provision Cloud Resources**  
   - Choose your cloud provider (Azure, AWS, GCP).  
   - Create a virtual machine or container instance with the required specifications (recommendations: 4 vCPU, 8GB RAM).  
   - Ensure the VM/container has internet access and open ports 80 (HTTP) and 443 (HTTPS).

2. **Configure the Database**  
   - Set up a SQL Server (Azure SQL, RDS, or self-hosted).  
   - Create a database named `TestWorthyDB`.  
   - Note the connection string for later use.

3. **Deploy Application Files**  
   - Clone the repository or copy the build output (from `dist/` or `build/`) to the server.  
   - Install dependencies:  
     ```bash
     npm install
     ```  
   - Build the application:  
     ```bash
     npm run build
     ```  
   - Configure environment variables or appsettings.json with your database connection string and other settings.

4. **Configure Web Server**  
   - Use IIS, Nginx, or Apache to serve the application.  
   - Set up HTTPS with SSL certificates.  
   - Configure reverse proxy if needed.

5. **Initialize the Database**  
   - Run migration scripts or use Entity Framework migrations to create schema:  
     ```bash
     dotnet ef database update
     ```  
   - Seed initial data if necessary.

6. **Start the Application**  
   - Run the app as a service or via `dotnet` CLI:  
     ```bash
     dotnet TestWorthy.dll
     ```  
   - Verify deployment by accessing the URL.

7. **Configure DNS and SSL**  
   - Point your domain to the cloud server IP.  
   - Set up SSL certificates for secure access.

8. **Monitor and Maintain**  
   - Use cloud monitoring tools for health checks.  
   - Set up backups for the database.

## On-Premises Installation

To install TestWorthy on your own servers:

1. **Prepare the Server Environment**  
   - Install Windows Server or Linux with .NET Core runtime installed.  
   - Install SQL Server or compatible database engine.

2. **Download Application Files**  
   - Clone the repository or download the latest release package.  
   - Extract files to a directory, e.g., `C:\TestWorthy` or `/opt/testworthy`.

3. **Configure Environment Settings**  
   - Edit `appsettings.json` with your database connection string and environment-specific parameters.  
   - Set environment variables if needed.

4. **Install Dependencies**  
   - Run:  
     ```bash
     dotnet restore
     ```  
   - Build the project:  
     ```bash
     dotnet build
     ```

5. **Apply Database Migrations**  
   - Run Entity Framework migrations:  
     ```bash
     dotnet ef database update
     ```  
   - Or run seed scripts if provided.

6. **Configure Web Server**  
   - Use IIS (Windows) or Nginx/Apache (Linux) to host the application.  
   - Set up a reverse proxy if necessary.  
   - Configure SSL certificates for HTTPS.

7. **Start the Application**  
   - Run as a Windows Service or Linux daemon:  
     ```bash
     dotnet TestWorthy.dll
     ```  
   - Ensure the application is accessible via the configured URL.

8. **Verify and Secure**  
   - Test access via browser.  
   - Configure firewall rules to restrict access.  
   - Set up regular backups for data.

9. **Maintain and Update**  
   - Regularly update dependencies and apply schema migrations.  
   - Monitor server health and logs.

**Tip:** Always test deployment in a staging environment before production.

---

This guide provides the essential steps to deploy TestWorthy either in the cloud or on-premises. Adjust configurations based on your infrastructure and security policies.