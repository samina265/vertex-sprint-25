# vertex-sprint-25
A simple agent who can provide the financial guideline as new comer 

---

## Project Title: **"Smart Financial Assistant Using Vertex AI & Gemini"**

### **Project Documentation**

#### **1. Project Overview**
The **Smart Financial Assistant** is an AI-powered agent that leverages **Google Vertex AI** and **Gemini API** to provide financial insights and assist users in decision-making.The primary goal of this project is to build a financial assistant that can analyze financial trends, answer queries, and help users make better financial decisions. 

At this stage, the project is in its **basic form**. Future improvements will include country specific data analysis, risk assessment, and automated investment advice so that a non financial expert can invest without any fear.


#### **2. Features**
- Uses **Google Vertex AI** for AI model management.
- Integrates **Gemini AI (function calling)** to process and respond to financial queries.
- Basic functionality for querying financial trends.
- **Scalable design** for future improvements such as financial risk assessment and portfolio management.
- Secure authentication using **Google Cloud authentication**.
- 
#### **3. Installation & Setup**
##### **Prerequisites**
- Google Cloud SDK installed
- Vertex AI enabled in the Google Cloud project
- Service account with necessary permissions

##### **Steps to Run the Project**
1. **Authenticate Google Cloud**
   ```bash
   gcloud auth application-default login --no-launch-browser
   ```

2. **Set the Google Cloud project**
   ```bash
   gcloud config set project <your-project-id>
   ```

3. **Initialize Vertex AI in Python**
   ```python
   from google.auth import default
   from vertexai import init

   credentials, project_id = default()
   init(project=project_id, location="us-central1", credentials=credentials)
   ```

4. **Initialize the Gemini AI Model**
   ```python
   from vertexai.generative_models import GenerativeModel, Content

   model = GenerativeModel("gemini-2.0-flash-001")
   user_query = "What is the latest trend in AI?"
   response = model.generate_content([Content(role="user", parts=[user_query])])
   print(response)
   ```

#### **4. Limitations**
1. **Limited Financial Insights**: The current version does not use real-time financial data or stock market trends.
2. **No Personalization**: The assistant does not yet provide personalized financial advice based on user data.
3. **Data Dependency**: Relies on AI-generated responses, which may not always be accurate or up-to-date.
4. **Security Concerns**: User authentication and sensitive data handling are not yet fully implemented.

#### **5. Future Enhancements**
- **Integration with real-time financial APIs** (Yahoo Finance, Alpha Vantage) for accurate market analysis.
- **Personalized financial planning** using user profiles and spending history.
- **Investment recommendations** based on AI-driven analysis.
- **Improved security measures** for handling user data and authentication.
- **Mobile and Web App Integration** for user-friendly access.

#### **6. How This Project Benefits Society**
1. **Financial Literacy**: Helps individuals understand financial trends and improve their knowledge.
2. **Investment Awareness**: Assists in making **data-driven** investment decisions.
3. **Accessibility**: Provides **free** financial insights without requiring expert consultations.
4. **Automation of Financial Queries**: Saves time by offering **instant AI-driven answers** to common financial questions.

__Thank You| Google ML Team_ 
