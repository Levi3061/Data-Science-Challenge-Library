---

# Data Science Challenge Library

A web-based platform for exploring data science competitions, submitting solutions, and viewing results on leaderboards. Additionally, the platform includes machine learning tools to predict tags for questions and assess their quality.

## Features

- **User Accounts:** Register and log in to access competitions and submit solutions.
- **Data Science Competitions:** Browse challenges, submit entries, and track your position on leaderboards.
- **Predictive Tools:**
  - **Tag Prediction:** Use a trained model to suggest relevant tags for a given question.
  - **Question Quality Assessment:** Evaluate the quality of a question using a pre-trained model.
- **File Uploads:** Upload supporting documents (e.g., PDFs) related to challenges or solutions.

## Technology Stack

- **Backend:** Node.js with Express
- **Frontend:** EJS templates, CSS
- **Machine Learning:** Python 3 scripts with pre-trained `.pkl` models
- **Additional Tools:** 
  - `question_quality_model.pkl` and `tag_predictor_model.pkl` for ML inference
  - `train_model.py` and `test.py` for training and testing models

## Project Structure

```
.
├─ public/                 # Static files (CSS, images)
├─ routes/
│  └─ auth.js             # Authentication routes
├─ uploads/               # Uploaded documents
├─ views/
│  ├─ index.ejs           # Home page
│  ├─ login.ejs           # Login form
│  ├─ registration.ejs    # Registration form
│  ├─ competitions.ejs    # List of competitions
│  ├─ leaderboard.ejs     # Leaderboards
│  ├─ predict_tags.ejs    # Tag prediction page
│  ├─ predictive_analysis.ejs # Question quality analysis
│  └─ partials/           # Reusable templates (header, footer)
├─ question_quality_model.pkl
├─ tag_predictor_model.pkl
├─ tag_binarizer.pkl
├─ question_quality_predictor.py
├─ train_model.py
├─ test.py
├─ secretkey.js            # Configuration or secret keys
├─ server.js               # Express server entry point
├─ package.json
└─ README.md
```

## Getting Started

### Prerequisites

- **Node.js & npm:** Ensure you have Node.js (version 12+) installed.
- **Python 3:** Required for model training or testing scripts.
- **Git (optional):** For version control and easy cloning.

### Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Levi3061/Data-Science-Challenge-Library.git
   cd Data-Science-Challenge-Library
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment (If Needed):**
   If the app uses secret keys (e.g., for sessions) defined in `secretkey.js` or environment variables, set them before running:
   ```bash
   export SESSION_SECRET="your_secret_key"
   ```

### Running the Application

Start the server:

```bash
npm start
```

Open your browser and go to `http://localhost:3000` (or the displayed port) to view the site.

### Using the Predictive Tools

- **Tag Prediction:**  
  Navigate to the tag prediction page (e.g., `/predict_tags` from the UI). Enter the question details, submit, and the model will suggest tags.

- **Question Quality Analysis:**  
  Similar to tag prediction, go to the quality analysis page (`/predictive_analysis`). Input your question and get a quality score.

### Training & Testing Models

- **Train Models:**
  ```bash
  python3 train_model.py
  ```
  Adjust this script as needed for your data and desired output.

- **Test Models:**
  ```bash
  python3 test.py
  ```
  Evaluate the model’s accuracy and performance.

## Contributing

1. **Fork the repository** on GitHub.
2. **Create a new branch** for your feature or bug fix:
   ```bash
   git checkout -b feature/my-new-feature
   ```
3. **Commit and push** your changes.
4. **Open a Pull Request** against the main branch.

## License

This project is available under the [MIT License](https://opensource.org/licenses/MIT). 
