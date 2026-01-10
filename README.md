# University Digital Notice Board A4

**Project:** University Digital Notice Board A4 — static website  
**Team Lead:** Khizra Jamshaid  
**Repo:** https://github.com/DevOpsG4Assignments/uni-notice-board.git

---

## Overview
This project is a static University Digital Notice Board website built collaboratively using Git/GitHub, GitHub actions and containerized with Docker. The site is built with Parcel, deployed into an Nginx container via a multi-stage Dockerfile and Docker image in CI pipelines. The project enforce HTML and CSS quality using HTMLHint and Stylelint.

## Structure
```
uni-notice-board/
├── .github/
│   └── workflows/
│       └── ci.yml
├── .gitignore
├── .dockerignore
├── .htmlhint.json
├── .stylelintrc.json
├── Dockerfile
├── package.json
├── README.md
├── src/
│   ├── index.html
│   ├── notices.html
│   ├── exams.html
│   ├── admissions.html
│   ├── academia-calendar.html
│   └── contact.html
└── styles/
    └── style.css
```


## Setup Instructions

### Clone the repository 
```bash
git clone https://github.com/DevOpsG4Assignments/uni-notice-board.git
cd uni-notice-board
```

### Install Node.js dependencies
Make sure you have Node.js installed. Then run:
```bash
npm install
```
### Lint HTML files in your code
```bash
npx htmlhint "**/*.html"
```
### Lint CSS files on your code
```bash
npx stylelint "**/*.css"
```
### Build your code
```bash
npx parcel build "./src/index.html" --dist-dir "./dist" --public-url "./" --no-cache
```