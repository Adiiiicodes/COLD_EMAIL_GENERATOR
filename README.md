## Cold Email Generator 🌌

The **Cold Email Synthesizer** is an AI-powered web application designed to help businesses generate tailored cold emails for outreach based on a provided context, job requirements, and portfolio. The app leverages advanced NLP (Natural Language Processing) techniques to extract information from webpages and generate effective emails using AI. It features a clean, user-friendly interface with custom styling for an engaging user experience.

---

## Key Features
- **Context Initialization**: Define your company's context, services, and offerings to guide email generation.
- **Portfolio Synchronization**: Upload your portfolio in CSV format to link relevant project experiences with job requirements.
- **AI-Driven Email Generation**: Automatically extract job requirements from a target webpage and generate a custom cold email.
- **Custom Styling**: A futuristic theme to make the interface visually appealing.
- **Error Handling**: Comprehensive error handling and logging to ensure a smooth user experience.

---

## Tech Stack
- **Frontend**:
  - [Streamlit](https://streamlit.io/) for the web interface and user interaction.
  - Custom CSS for a unique and engaging user experience.
  
- **Backend**:
  - **Python**: Core language for logic and AI integration.
  - **LangChain**: For AI processing and job requirement extraction.
  - **ChromaDB**: As a vector database for storing and querying skills and portfolios.
  - **WebBaseLoader**: For extracting webpage content.

- **File Handling**:
  - `Pandas`: For processing uploaded CSV files and portfolio data.
  - `io` and `csv`: For handling file uploads and downloads.

---

## Installation Guide
Follow these steps to set up the Cold Email Synthesizer locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/cold-email-synthesizer.git
   cd cold-email-synthesizer
   ```

2. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**:
   ```bash
   streamlit run app.py
   ```

5. **Access the Application**:
   - Open your browser and navigate to `http://localhost:8501`.

---

## User Guide

### Step 1: Context Initialization
1. Open the application in your browser.
2. Navigate to the **Configuration Matrix** tab.
3. Provide a detailed description of your company and its offerings in the **"Initialize Your Context"** text area.  
   Example:  
   ```
   We are AdityaTechLabs, a leading AI consulting firm specializing in automation and process optimization for businesses of all sizes.
   ```

4. Optionally, click the **"Access Example Context"** button to load a pre-defined example.

### Step 2: Portfolio Synchronization
1. Upload your portfolio file in CSV format via the **"Upload Your Portfolio"** section.
   - File format:  
     ```
     Techstack,Links
     React | Node.js | MongoDB,https://example.com/react-portfolio
     Angular | .NET | SQL Server,https://example.com/angular-portfolio
     ```
2. Ensure the file contains two columns:
   - `Techstack`: Technologies used in the project, separated by `|`.
   - `Links`: URL pointing to the project details.

3. Review errors, if any, and correct the file before re-uploading.
4. Once uploaded successfully:
   - Preview and edit the data in the **Portfolio Preview** section.
   - Click **"Commit Synchronization"** to save the portfolio data.

5. Download the example portfolio template if needed by clicking **"Download Example Template"**.

### Step 3: Email Generation
1. Switch to the **Email Synthesizer** tab.
2. Enter the target webpage URL where job requirements are listed.
   - Example: `https://example.com/job-posting`
3. Click **"Synthesize Email"**.
   - The AI will:
     - Extract job details from the URL.
     - Match job requirements with your portfolio.
     - Generate a cold email using the context and matched portfolio items.
4. Review the generated email under the **"Synthesized Cold Email"** section.
5. Copy the email for use.

---

## Example Use Case
**Scenario**:  
AdityaTechLabs wants to apply for a project requiring AI-based process automation.  

1. **Context**:  
   ```
   We are AdityaTechLabs, experts in AI automation solutions for medium to large enterprises. Our solutions reduce operational costs by up to 40%.
   ```
2. **Portfolio**:  
   - Uploaded a CSV with projects in AI, automation, and software development.
3. **Target URL**:  
   `https://client-website.com/ai-project-requirements`
4. **Outcome**:  
   - Generated an email emphasizing AdityaTechLabs' expertise in automation, referencing relevant portfolio projects.

---

## Troubleshooting

1. **Error: "Portfolio Synchronization Failed"**:
   - Ensure the uploaded file has exactly two columns: `Techstack` and `Links`.
   - Ensure the `Techstack` field contains technologies separated by `|`.
   - Ensure the `Links` field contains valid URLs.

2. **Error: "Target Web Page URL Required"**:
   - Verify that you have entered a valid URL in the target URL field.

3. **"No Jobs Could Be Extracted" Warning**:
   - Check the target webpage URL to ensure it contains clear job descriptions.

4. **General Issues**:
   - Check the application logs for detailed error messages.
   - Ensure all dependencies are installed and up to date.


---

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or features.

## 📫 Reach Out

Developed by [Aditya Nalawade](https://www.linkedin.com/in/aditya-nalawade-a4b081297) | [GitHub](https://github.com/Adiiiicodes)
