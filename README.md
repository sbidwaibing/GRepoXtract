# 🚀 GRepoXtract 
### the ultimate GitHub Project Data Extractor

## Overview
This script automates the process of fetching all repositories from a GitHub account, extracting their descriptions, technologies used, and full README content. The data is saved in a structured text file for easy reference.

## Features
- Fetches **all repositories** from a GitHub account.
- Extracts:
  - Repository **name**
  - Repository **description**
  - **Languages/Technologies** used
  - **Full README** content (no size limit)
- Saves the extracted information in a structured **text file**.
- **Google Colab Compatible**
- **Auto-downloads** the output file.

## Requirements
- A **GitHub account**
- A **GitHub Personal Access Token (PAT)**
- Google Colab (or a local Python environment with `requests` installed)

## How to Generate a GitHub Personal Access Token (PAT)
### 1. Navigate to GitHub Developer Settings
- Go to **GitHub** and sign in.
- Visit **[GitHub Token Settings](https://github.com/settings/tokens)**

### 2. Generate a New Token
- Click **"Generate new token"**.
- If using **Fine-grained tokens**, select **"Repository Access"** and specify the repositories.
- If using **Classic tokens**, choose:
  - `repo` (Full control over private repositories, if needed)
  - `read:repo` (Read-only access for repositories)
  - `read:user` (To access user profile data)
  
### 3. Copy and Store the Token Securely
- **Copy the generated token** and store it securely.
- **GitHub will not show it again!**

## Usage Instructions
1. **Install Dependencies** (If running locally, skip if using Google Colab)
   ```python
   !pip install requests
   ```

2. **Run the Script in Google Colab**
   - Copy and paste the provided Python script into a Google Colab notebook.
   - Replace `GITHUB_USERNAME` and `GITHUB_TOKEN` in the script with your credentials.
   - Run the script to fetch and save project data.

3. **Download the Generated File**
   - The script automatically saves the extracted data as `github_projects.txt`.
   - The file will be **downloaded automatically** to your system.

## Output Format
The generated text file contains:
```
📌 Repository: <Repository Name>
📖 Description: <Description>
💻 Technologies Used: <Languages>

📜 README Content:
<Full README.md Content>

================================================================================
```
Each repository's data is separated by a line for readability.

## Notes
- If a repository **does not have a README**, it will indicate `No README available`.
- If the token has insufficient permissions, the script may fail to fetch data.
- Ensure your **token has `read:repo` permissions** to access private repositories.

---

Enjoy automating your GitHub project documentation! 🚀
