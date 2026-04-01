# AI Interview Coach
An AI-powered interview simulator build with Streamlit and OpenAI that helps users practice real interview scenarios, receive structured feedback, and improve their performance.

## Features
### Personalized Interview Setup
- Input you **name, experience, and skills**
- Select:
    - Experience Level (Junior, Mid-Level, Senior)
    - Target Role
    - Company Name 

### Real-Time Interview Simulation
- AI acts as the **HR interviewer**
- Generated dynamic, context-aware questions
- Simulates a realistic interview flow
- Limited to 5 responses for structured sessions

### AI-Powered Feedback
- After the interview, receive:
    - **Score (1-10)**
    - Strengths and Weeknesses
    - Suggestions for improvement

### Sesion Management
- Maintains conversation using Streamlit sesstion state
- Restart interview instantly

## Tech Stack
- **Frontend/UI:** Streamlit
- **Backend:** Python
- **AI Engine:** OpenAI API (`gpt-4o`)
- **State Management:** Streamlit Sesstion State
- **Streaming Responses:** OpenAI streaming API

## Installation
 1. Clone the Repository
 ```bash
 git clone https://github.com/Drew-Andersen/Interview-tool.git
 cd Interview-tool
 ```

 2. Create a virtual environment
 ```bash
python -m venv venv
source venv/bin/activate #For Mac and Linux users
venv\Scripts\activate #For Windows users
 ```

 3. Install the dependancies
 ```bash
pip install -r requirements.txt
 ```

 4. Add your OpenAI API Key
 Create a .streamlit/secrets.toml file
 ```toml
 OPENAI_API_KEY = "you_api-key_here"
 ```

## Running the App
```bash
streamlit run app.py
```
Then open the loacl URL in your browser.

## How it Works
1. Fill out your personal and job details
2. Start the interview
3. Answer AI-generated questions
4. Complete 5 responses
5. Receive a score and feedback

## AI Prompt Design
### Interview Behavior
The AI is instructed to:
- Act as an HR interviewer
- Tailor questions based on:
    - Candidate profile
    - Role and company
    - Experience level

### Feedback System
- Evaluates full conversation history
- Returns:
    - Overall Score (1-10)
    - Structured feedback only (no follow-up questions)

## Project Structure
```
Interview-tool/
│── app.py
│── requirements.txt
│── .streamlit/
│   └── secrets.toml
│── README.md
```

## Linitations
- Fixed to 5 interview responses per session
- No persistant storage (sesstion resets on refresh)
- Text-based only (no voice support yet)

## Future Improvements
- Voice-based interview mode
- Resume upload for tailored questions
- Detailed analytics dashboard
- Role-specific technical interviews (coding, SQL, etc.)
- Database for tracking progress over time

## Contributing
Contributions are welcome!
1. Fork the repo
2. Create a feature branch
3. Submit a pul request

## Author
Drew Andersen

## Support
If you found this project helpful, consider giving it a ⭐️ on GitHub!