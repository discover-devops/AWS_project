### **"Build and Secure a Scalable Blogging Platform on AWS"**

#### **Project Overview**
Students will design, deploy, and secure a scalable blogging platform using AWS services: **EC2**, **Elastic Beanstalk (EBS)**, **RDS**, **S3**, and **IAM**. The project will involve setting up the infrastructure, hosting a web application, managing a database, storing media files, and implementing security best practices. This project mimics real-world scenarios and will take approximately **20 hours** to complete.

---

### **Project Objectives**
1. Deploy a web application for blogging on **Elastic Beanstalk (EBS)**.
2. Set up a **MySQL database** on **RDS** for storing user data and blog content.
3. Use **S3** to store and serve static content like images and CSS files.
4. Configure an **EC2 instance** to serve as a bastion host for database access.
5. Implement fine-grained **IAM** roles and policies to secure the application and resources.
6. Use versioning and lifecycle policies on **S3** for data management.
7. Implement logging and monitoring.

---

### **Detailed Steps**

#### **Part 1: Deploy the Web Application**
1. **Setup Elastic Beanstalk (EBS)**:
   - Create an Elastic Beanstalk application and deploy a sample **Node.js**, **PHP**, or **Python** blogging application.
   - Configure the environment to use **Elastic Load Balancer** and **Auto Scaling** for high availability.
   - Connect the application to an **RDS MySQL database** (created in Part 2).

2. **Create an EC2 Bastion Host**:
   - Launch an EC2 instance in a public subnet.
   - Configure the bastion host for SSH access to the RDS database securely.

#### **Part 2: Set Up the Database**
1. **Launch an RDS MySQL Instance**:
   - Create a new RDS instance with MySQL.
   - Configure a security group to allow access only from the EC2 bastion host and Elastic Beanstalk environment.

2. **Database Schema**:
   - Create a schema to store user information, blog posts, and metadata.
   - Use the provided SQL script to create tables and insert sample data.

#### **Part 3: Store Static Content on S3**
1. **Create an S3 Bucket**:
   - Create an S3 bucket to store images, videos, and static files for the blogging platform.
   - Enable **versioning** and set up a **lifecycle policy** to move older files to **Glacier** after 30 days.

2. **Static Content Delivery**:
   - Configure the application to upload and retrieve images from the S3 bucket using SDKs (e.g., AWS SDK for Python or JavaScript).

#### **Part 4: Secure the Application**
1. **Configure IAM Roles and Policies**:
   - Create an IAM role for the Elastic Beanstalk application with S3 read/write access.
   - Create an IAM role for the EC2 bastion host with permissions to access the RDS database.

2. **Security Best Practices**:
   - Use **KMS** to encrypt sensitive data in RDS and S3.
   - Restrict inbound and outbound traffic using **security groups**.

#### **Part 5: Enable Monitoring and Logging**
1. **Enable CloudWatch Metrics and Logs**:
   - Configure the application logs to stream to **CloudWatch Logs**.
   - Set up CloudWatch alarms for critical metrics like CPU utilization and RDS storage space.

2. **Access Logs**:
   - Enable access logging for the S3 bucket and Elastic Load Balancer.

---

### **Deliverables**
1. **Architecture Diagram**: Include a simple diagram showing all components and their interactions.
2. **Screenshots**: Provide screenshots of the Elastic Beanstalk environment, RDS instance, EC2 bastion host, S3 bucket policies, and IAM roles.
3. **Database Schema**: Submit the SQL scripts used for creating the database schema and sample data.
4. **Web Application Code**: Submit the code for the blogging application (starter template can be provided).
5. **Documentation**: A detailed step-by-step guide explaining how each component was configured.

---

### **Skills Covered**
- Deploying applications on Elastic Beanstalk
- Database management with RDS
- Storing and managing files with S3
- Configuring IAM roles and policies for security
- Monitoring and logging with CloudWatch
- Networking and secure access using EC2 instances

---

### **Estimated Time Breakdown**
| Task                                   | Estimated Time |
|----------------------------------------|----------------|
| Elastic Beanstalk setup                | 4 hours        |
| RDS setup and configuration            | 3 hours        |
| EC2 bastion host setup                 | 2 hours        |
| S3 bucket setup and integration        | 3 hours        |
| IAM roles and policies configuration   | 3 hours        |
| Monitoring and logging                 | 2 hours        |
| Testing and debugging                  | 3 hours        |

---


