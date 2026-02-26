# Black Board Quiz to Anki 🧑‍🏫📥

Makes student life easier by converting Black Board quizzes to Anki flashcards. Save time and get better grades!

## Install

# Clone the repository
1. git clone https://github.com/AlppOz/BlackBoardtoAnki

# Navigate to the cloned directory
2. cd BlackBoardtoAnki

# Install required packages
3. pip install -r requirements.txt

Note: Ensure that the Python scripts are added to PATH



## Usage

# Locally host the main website from your terminal
1. streamlit run website/main.py

# Open a Blackboard quiz attempt (can do an empty attempt if you need)
# Inspect elements and open the console and paste
2. let params=new URLSearchParams(window.location.search),course=window.location.pathname.split("/")[3],attempt=params.get("attemptId"),url=window.location.origin+"/learn/api/v1/courses/"+course+"/gradebook/attempts/"+attempt+"/assessment/answers/grades?expand=questionAttempt.question,questionAttempt.answerCorrectness";fetch(url).then(r=>r.json()).then(data=>{console.log(data);let blob=new Blob([JSON.stringify(data)],{type:"application/json"});window.open(URL.createObjectURL(blob))}).catch(e=>console.error(e));

# Copy the .json text and paste it to the locally running website
# Download the Anki file produce



## Downloading Quizes
This algorithm makes use of [browser-hook](https://github.com/velocitatem/browser-hook) to download the quizes, you can find some boiler plate in `main.py`.
