# llm-release-notes-generator
This project automates the generation of release notes using GitHub Actions and AI.

Whenever a pull request is merged:
- The PR diff is fetched
- AI summarizes the changes
- A GitHub Release is created or updated automatically

No manual changelog writing required.

## 🔐 Setup (API Keys)

This project uses AI to generate release notes, so you need to add an API key.

To make it work:

- Go to your repository → **Settings → Secrets and variables → Actions**
- Click **New repository secret**
- Add the following:

  OPENROUTER_API_KEY = your_api_key

This key is used to call the AI model for summarizing pull requests.

GitHub automatically provides a built-in token (`GITHUB_TOKEN`) for accessing repository data, so you don’t need to configure that manually.

