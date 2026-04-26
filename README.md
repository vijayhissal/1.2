STEP 1: Create Simple Flask Project
 app.py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello DevOps"

if __name__ == '__main__':
    app.run(debug=True)
 requirements.txt
Flask
 STEP 2: Initialize Repository & Push
git init
git add .
git commit -m "Initial Flask project"
git branch -M main
git remote add origin https://github.com/your-username/flask-app.git
git push -u origin main

 Say:

“This initializes repository and pushes project to GitHub.”

 STEP 3: Create Branch
git branch feature1
git checkout feature1

👉 OR:

git checkout -b feature1
 STEP 4: Make Changes in Branch

Edit app.py:

return "Hello DevOps - Feature Added"

Then:

git add .
git commit -m "Added feature in branch"
git push origin feature1
 STEP 5: Merge Branch

Switch to main:

git checkout main
git merge feature1
git push origin main

 Say:

“Branch changes are merged into main branch.”

 STEP 6: View Commit History
git log --oneline

 Shows:

Commit ID
Messages
 STEP 7: Revert Changes

 Get commit ID from log

git revert <commit-id>
git push

 Say:

“This safely undoes changes without deleting history.”

 STEP 8: Demonstrate Collaboration Workflow

 Simulate 2 developers:

 Developer 1
Push code to GitHub
 Developer 2 (or same system)
git clone https://github.com/your-username/flask-app.git
cd flask-app
git checkout -b feature2

Make changes → then:

git add .
git commit -m "Feature 2 added"
git push origin feature2
 Merge Collaboration
git checkout main
git merge feature2
git push origin main
🔄 WORKFLOW (Explain this)
Developer → GitHub → Branch → Commit → Merge → Update
