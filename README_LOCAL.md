# Grama-Vaxi Local Setup Guide

If you have downloaded the code and want to run it on your own computer using a terminal, follow these steps:

## Prerequisites
- **Node.js**: Make sure you have Node.js installed (v18 or higher is recommended).
- **Terminal**: Use Command Prompt, PowerShell, or any terminal.

## Steps to Run
1. **Unzip the folder**: Extract the contents of the zip file.
2. **Open Terminal**: Navigate to the folder where you extracted the files.
   ```bash
   cd Grama-Vaxi
   ```
3. **Install Dependencies**: Run the following command to download the necessary libraries.
   ```bash
   npm install
   ```
4. **Set Environment Variables**: 
   The app uses the Gemini API. You should have a `.env` file in the root directory with your API key:
   ```env
   GEMINI_API_KEY=your_actual_key_here
   ```
5. **Start the Development Server**: Run this command to start the app.
   ```bash
   npm run dev
   ```
6. **Open in Browser**: The terminal will show a link (usually `http://localhost:3000`). Ctrl+Click or copy-paste it into your browser.

## Troubleshooting
- If you see "npm is not recognized", you need to install [Node.js](https://nodejs.org/).
- If the app is blank, check the browser console (Press F12 -> Console) for any errors.
