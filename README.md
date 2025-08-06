Lumix - Your AI-Powered GitHub Assistant
Welcome to Lumix. This project is an intelligent GitHub assistant designed to supercharge your workflow. Instead of manually digging through repositories, Lumix allows you to use natural language to find files, view code, and even make edits on the fly, all from a clean, modern dashboard.

The core of Lumix is its AI-powered search. You can ask it to "find all CSS files" or "show me the database configuration," and it will search across all your repositories to find exactly what you are looking for.

Features
Secure GitHub Authentication: Connects to your GitHub account safely using the official OAuth2 flow. Your credentials are never stored.

Centralized Dashboard: View and browse all your repositories from a single, interactive sidebar.

AI-Powered Search: Uses the Google Gemini API to understand natural language queries and find files across all your projects.

Integrated Code Editor: Open, view, and edit any file directly within the application in a full-screen modal.

Direct Commits: Save your edits by committing them back to your GitHub repository with a custom message, right from the editor.

Light & Dark Modes: A sleek user interface with theme support to match your preference.

Tech Stack
Backend: Node.js, Express.js

Frontend: HTML5, CSS3, Vanilla JavaScript

Authentication: OAuth2, Express Session

APIs: GitHub API, Google Gemini API

Getting Started
Getting Lumix up and running on your local machine is straightforward. Here’s how you can do it:

1. Prerequisites
Make sure you have Node.js installed on your system. You can check by running node -v in your terminal.

2. Installation & Configuration
Clone the repository:

Bash

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Install dependencies:

Bash

npm install
This will install all the necessary packages listed in package.json.

Create your environment file:
Create a file named .env in the root of the project and add the following variables. You will need to get these credentials from GitHub and Google.

Code snippet

# GitHub OAuth App Credentials
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret

# Google Gemini API Key
GEMINI_API_KEY=your_gemini_api_key
3. Acquiring Credentials
GitHub Credentials:

Go to your GitHub Settings > Developer settings > OAuth Apps.

Click "New OAuth App".

Fill in the application details. For the "Authorization callback URL", you must use http://localhost:3000/callback.

After creating the app, generate a new client secret. Copy the Client ID and the new Client Secret into your .env file.

Gemini API Key:

Go to the Google AI Studio.

Click "Get API key" and create a new API key.

Copy the key and paste it into your .env file.

Usage
Once you have completed the setup, you can start the server:

Bash

node server.js
The application will be running at http://localhost:3000. Open this URL in your browser, log in with your GitHub account, and start exploring your repositories.
