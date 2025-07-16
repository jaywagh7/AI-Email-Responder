# 📧AI-Email-Responder

A Streamlit application that automatically processes and generates professional responses to emails using AI.
The app leverages LangChain, Groq, and Tavily for understanding, research, and response generation.

🚀 Key Features
✅ Email Categorization:
Automatically categorizes emails into specific types like price inquiries, complaints, product queries, feedback, or off-topic.

✅ Automatic Research:
Fetches additional information when needed (like product details or facts) using the Tavily API.

✅ Professional Response Generation:
Crafts polished and context-aware responses using the Groq API.

✅ Streamlit Interface:
Easy-to-use web app where you can input emails, preview categorization & research, edit drafts, and send emails — all in real-time.

🗂️ Project Structure
```bash
.
├── app.py                 # Main Streamlit app
├── .env                   # (Ignored) Your API keys and email credentials
├── .env.example           # Example env file with placeholders
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
├── notebook/              # Jupyter notebooks (optional)
├── outputs/               # Generated outputs (drafts, research, etc.)
├── src/                   # Main application logic
│   ├── chains.py
│   ├── config.py
│   ├── processors.py
│   ├── prompts.py
│   ├── state.py
│   └── workflow.py
├── utils/                 # Utility scripts
└── venv/                  # Python virtual environment
```

🛠️ Setup
1️⃣ Clone the repository
```bash
git clone https://github.com/jaywagh7/AI-Email-Responder.git
cd AI-Email-Responder
```
2️⃣ Create and activate a virtual environment
```bash
# Install virtualenv if you don't have it
pip install virtualenv

# Create a virtual environment
virtualenv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Mac/Linux)
source venv/bin/activate
```
3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

4️⃣ Create .env file
Copy .env.example to .env and fill in your credentials:
```bash
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=465
EMAIL_USE_SSL=true
EMAIL_HOST_USER=youremail@example.com
EMAIL_HOST_PASSWORD=your_email_password
EMAIL_FROM=youremail@example.com
```

📈 Run the App
```bash
streamlit run app.py
```

✨ Usage
1️⃣ Enter the incoming email content in the text area.
2️⃣ Enter the recipient’s email address.
3️⃣ Click Generate Response & Send.
4️⃣ Review the response:

Edit it if needed.
Preview it.
Save draft.
Send again if needed.

5️⃣ Previous drafts and responses are saved in history.

📋 Notes
Your .env file is ignored in .gitignore so your secrets stay safe.
Do not commit .env to your repository.
You can edit the name, templates, or prompts in src/prompts.py to customize responses.

🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

