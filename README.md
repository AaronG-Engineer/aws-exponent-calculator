# 🧮 Power of Math – Serverless Exponent Calculator

This project is a simple serverless web application built on AWS that calculates exponents (base^exponent). The core idea: spin up a full-stack application using modern AWS services—with no frameworks or boilerplate—just raw cloud building blocks and problem-solving.

---

## 🚀 What It Does

The user enters a **base** and **exponent** in a web interface. Those values are sent to a **Lambda function**, which calculates the result and stores it in a **DynamoDB** table. The result is returned to the webpage and displayed instantly.

---

## ⚙️ Tech Stack

- **Frontend:** Static HTML/CSS, hosted on **AWS Amplify**
- **Backend:** **AWS Lambda** function for math logic
- **API Gateway:** Public HTTP endpoint to trigger Lambda
- **Database:** **DynamoDB** table for result persistence
- **IAM:** Fine-tuned permissions for Lambda to access DynamoDB (`PutItem`, `GetItem`, `UpdateItem`)

---

## 🧱 How I Built It – Step-by-Step

1. **Hosted the Website (Amplify)**
   - Created a simple HTML webpage using Notepad++.
   - Compressed into a `.zip` file and deployed with AWS Amplify.
   - Updated the HTML later with buttons, styles, and basic form inputs.

2. **Built the Lambda Function**
   - Wrote a basic Node.js function to compute `base^exponent`.
   - Tested it in the Lambda console with mock events.
   - Configured IAM permissions to interact with DynamoDB.

3. **Integrated API Gateway**
   - Created a REST endpoint:
     ```
     https://f52rlmaud4.execute-api.us-east-2.amazonaws.com/dev
     ```
   - Hooked it up to the Lambda to allow web calls.

4. **Created DynamoDB Table**
   - Table name: `powerofmathdb`
   - Lambda stores each operation’s result with input metadata.

5. **Connected Everything in HTML**
   - Used JavaScript `fetch()` in `index.html` to POST base and exponent values.
   - Displayed the response (answer) dynamically in the UI.
   - Styled the page with colors, spacing, and simple UI layout.

---

## 📓 UI Differences from the Course

This project followed an older AWS course from 2022. A couple of the Amplify UI steps had changed:

- The course said to **drag and drop HTML into the Amplify console** for updates. In the current version, I had to go to the **“Deploy update”** section and manually hit **Save + Deploy**.
- Also, what used to auto-deploy now required explicit deployment after uploading changes.

Not major issues, but worth noting—I had to adapt slightly to get things working.

---

## ✅ Final Thoughts

This was a great hands-on refresher in deploying AWS serverless architecture manually. I handled IAM policies, connected services across regions, debugged UI changes, and walked away with a better sense of how AWS services fit together.

The whole setup is deleted now since this was a test environment—but I kept these notes (and screenshots) so I can rebuild it again or show how I troubleshoot and document cloud projects in real life.
