# amc-adaptive
AMC Adaptive Practice

A free, open-source practice tracker for AMC and AIME students. Log your attempts, get an estimate of your current skill, and get a suggestion for the next problem at the right difficulty. It runs entirely in your browser: no account, no server, no data collection.

Live site: https://2029grad.github.io/amc-adaptive/

Status: v0, in active development. See the checklist below for what works today.

Why this exists

Most AMC/AIME prep is "do a past test, check the answers, repeat." That treats every problem as equally useful, but a problem that is far too easy or far too hard teaches you little. This tool estimates your skill from your own results and picks problems near the edge of what you can solve.

How it works
1. You log each attempt: which problem, whether you solved it, how long it took, and how much help you used.
2. The tool estimates your skill using a Rasch model (a simple item response theory model). The probability that you solve a problem is P(solve) = 1 / (1 + exp(-(skill - difficulty))) and your skill estimate is the value that makes your logged results most likely (maximum likelihood).
3. It suggests the unattempted problem whose difficulty is closest to your current estimate.

Difficulty is currently a rough 1 to 5 rating based on a problem's position in the test. Calibrating difficulty from real user data is a planned improvement.

Features
 Live page on GitHub Pages
 Problem list (IDs and links only)
 Attempt log, saved in your browser
 Skill estimate (Rasch maximum likelihood)
 "Suggest next problem" button
 CSV export of your attempts
 AIME problems
 Difficulty calibrated from user data
 
How to use it
1. Open the live site.
2. Pick a problem from the list and open its AoPS link to solve it.
3. Log whether you solved it, how many minutes it took, and what hints you used.
4. After a few attempts, click Suggest next problem.

Privacy

Your attempts are stored in your browser's local storage on your own device. Nothing is sent anywhere, and there is no account. Clearing your browser data erases your history, so use the CSV export to keep a copy.

About the problem data

This repo stores only problem IDs (for example 2023-10A-12), links to the Art of Problem Solving wiki, and my difficulty ratings. It does not reproduce problem text, which is copyrighted by the Mathematical Association of America. Problem statements and solutions live on the AoPS wiki.

Project files
index.html
problems.json	
BUILD_LOG.md

Feedback
Found a bug or have an idea? Open an issue on this repo.

Author
Built by Pratham Prasanna, a student at Bellarmine College Prep, as part of independent work on adaptive experimentation for AI-assisted learning.
