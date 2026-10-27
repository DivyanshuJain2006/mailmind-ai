📧 Email Agent using LangChain

An AI-powered Email Agent built using LangChain, LangGraph, Groq, and Streamlit that helps users compose and send emails through a conversational interface.

🚀 Features

* 💬 Interactive chat interface using Streamlit.
* 🤖 AI-powered email assistance using LangChain and Groq.
* ✉️ Send emails to specified email addresses using Gmail SMTP.
* 🔐 Store email credentials securely using environment variables.
* 🧠 Maintain conversation state using LangGraph’s in-memory checkpointer.

🛠️ Tech Stack

* Python
* LangChain
* LangGraph
* Groq
* Streamlit
* SMTP (Gmail)
* python-dotenv

📁 Project Structure

03_email_agent/
├── app.py
├── agent.py
├── tools.py
├── .env
├── .gitignore
└── requirements.txt

Note: .env contains sensitive credentials and must not be committed to GitHub.

⚙️ Installation and Setup

1. Clone the repository

git clone https://github.com/YOUR_USERNAME/email-agent.git
cd email-agent

Replace YOUR_USERNAME with your GitHub username.

2. Create a virtual environment

python -m venv .venv

Activate it on macOS or Linux:

source .venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

4. Configure environment variables

Create a .env file in the project root:

MODEL=your_groq_model_name
SENDER_EMAIL=your_email@gmail.com
SENDER_PASSWORD=your_gmail_app_password

Replace the example values with your actual configuration.

* MODEL: A Groq-supported model compatible with your installed LangChain integration.
* SENDER_EMAIL: Your Gmail address.
* SENDER_PASSWORD: Your Gmail App Password.

Never upload your .env file or share your credentials publicly.

5. Configure Gmail

To send emails through Gmail SMTP:

1. Enable 2-Step Verification on your Google account.
2. Generate an App Password if your account is eligible.
3. Store the App Password in your .env file.

6. Run the application

streamlit run app.py

The application should open in your browser.

🔄 How It Works

1. The user enters a request in the Streamlit chat interface.
2. The LangChain agent processes the request.
3. The agent gathers the recipient and email details.
4. The agent uses the email tool to send an email through Gmail SMTP.
5. The response is displayed in the chat interface.

🔒 Security Notes

* Never commit .env or other files containing secrets.
* Use environment variables for sensitive configuration.
* Review email details carefully before sending.
* For production use, implement explicit approval checks before allowing the agent to send an email.