"# Git Assignment" 

all commands

mkdir advanced-git-workflow
cd advanced-git-workflow
git init

echo "# Git Assignment" > README.md
git add .
git commit -m "Initial commit"

git branch -M main

git checkout -b develop
git checkout -b feature/login

git checkout develop
git checkout -b feature/payment

git checkout develop
git checkout -b feature/profile

git checkout develop
git checkout -b bugfix/login-error

git checkout feature/payment
echo "payment code" > payment.txt
git add .
git commit -m "Add payment feature"

git checkout develop
git merge feature/payment

git checkout feature/profile
echo "profile code" > profile.txt
git add .
git commit -m "Add profile feature"

git rebase develop

git checkout develop
git merge feature/profile

git checkout feature/login

echo "Login UI initialized" > login.txt
git add . && git commit -m "login UI"

echo "Added input validation (email & password)" >> login.txt
git add . && git commit -m "validation added"

echo "Fixed validation edge case for empty input" >> login.txt
git add . && git commit -m "bug fix"

echo "Enhanced UI with better layout and styling" >> login.txt
git add . && git commit -m "UI improved"

echo "Optimized login flow and finalized implementation" >> login.txt
git add . && git commit -m "final login"

git rebase -i HEAD~5

git log --oneline --graph

git remote add origin https://github.com/your-username/advanced-git-workflow.git

git push -u origin main
git push origin develop
git push origin feature/login
git push origin feature/payment
git push origin feature/profile
git push origin bugfix/login-error
