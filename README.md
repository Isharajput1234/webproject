🚀 AI-Powered Job Portal

This project is a full-stack recruitment platform built using Django and MySQL. It is designed to intelligently connect job seekers with employers using a machine learning–based recommendation system.

The platform goes beyond traditional job portals by introducing a Match Score mechanism, which evaluates how well a candidate fits a job role based on their skills and experience.

📌 Project Concept

Traditional job portals rely on manual search and keyword filtering. This project improves that process by:

Automatically analyzing user profiles and job descriptions
Generating a match percentage using AI
Helping users focus only on relevant job opportunities

The result is a faster and more efficient recruitment process.

🏛️ System Architecture

The project follows the MVT (Model-View-Template) architecture of Django, ensuring modular and scalable development.

🔹 Models (Data Layer)
Managed using Django ORM
Handles database structure and relationships
Key entities:
User (Custom authentication)
Job Seeker Profile
Employer Profile
Job Listings
Applications
🔹 Views (Logic Layer)
Handles core application logic
Uses:
Function-Based Views (for authentication workflows)
Class-Based Views (for dashboards and listings)
🔹 Templates (Presentation Layer)
Dynamic frontend built using HTML and Tailwind CSS
Provides separate dashboards for:
Job Seekers
Employers
🧠 AI Recommendation System

The core innovation of this project lies in its intelligent recommendation engine, implemented using Scikit-Learn.

⚙️ Working Process
Data Collection
Extracts text from:
User skills and experience
Job descriptions
Text Processing
Converts text into numerical form using TF-IDF Vectorization
Assigns higher importance to relevant technical keywords
Similarity Calculation
Uses Cosine Similarity to compare user profile and job description
Match Score Generation
Produces a score between 0 and 1:
1.0 → Highly relevant
0.0 → No relevance
Result Display
The score is shown as a percentage on the user dashboard

This allows users to prioritize jobs that best match their profile.

📂 Core Modules
🔹 Accounts Module
Manages user authentication and profiles
Supports two roles:
Job Seeker
Employer
🔹 Jobs Module
Handles job posting and application system
Tracks application status:
Pending
Accepted
Rejected
🔹 Dashboard Module
Provides personalized dashboards for both user types
Displays:
Recommended jobs
Application history
Match scores
📧 Automation System

The project uses Django Signals to automate workflows:

When an employer updates application status:
A signal is triggered
An email is automatically sent to the candidate using SMTP

This ensures real-time communication without manual intervention.

🔐 Security Features
Protection against SQL Injection (via Django ORM)
CSRF protection for secure requests
Secure password hashing using industry standards
🔑 OTP Verification System

A secure email-based OTP system is implemented for account verification:

Generates a 6-digit One-Time Password
Sent via email during registration
Ensures authenticity of user accounts
🎯 Key Highlights
Integration of Web Development and Machine Learning
Intelligent job recommendation system
Clean and scalable architecture
Real-world recruitment workflow implementation
