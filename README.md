# 📌 AI Feedback Automation Bot

## 📖 Description  
This project is an automated feedback collection and reporting system designed for educational environments. It allows students to submit complaints or feedback about teachers through a Google Form, and automatically generates weekly summarized reports for each teacher.

The system is designed to be dynamic and scalable — new teachers can be added without modifying the core automation logic.

---

## 🚀 Features  
- 📋 Google Form for student feedback submission  
- 📅 Automated weekly form open/close using Google Apps Script  
- 📊 Centralized data storage in Google Sheets  
- 🤖 AI-generated summaries of complaints per teacher  
- 📧 Automated email delivery of weekly reports to each teacher  
- ➕ Easy teacher onboarding via registry sheet (no code changes required)  

---

## 🏗️ System Workflow  
1. Students fill out a Google Form and select a teacher  
2. Responses are stored in a Google Sheet  
3. A teacher registry sheet maps teachers to their emails  
4. At the end of the week:
   - Form is closed for the week
   - UiPath automation is triggered  
   - Feedback is filtered teacher-wise  
   - AI generates summaries  
   - Emails are sent to respective teachers
   - Form is open for the new week   

---

## ⚙️ Tech Stack  
- UiPath (Automation)  
- Google Forms  
- Google Sheets  
- Google Apps Script  
- Generative Content (for summarization)  

---

## 📂 System Design Principle  
The system is built with **flexibility and maintainability** in mind:
- No hardcoded teachers  
- Dynamic data handling  
- Easy scaling by updating the registry sheet only  

---
