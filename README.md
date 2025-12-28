## Hi there 👋
.github/workflows
snake.yml
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"   # runs daily
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake animation
        uses: Platane/snk@v3
        with:
          github_user_name:apoorvd06
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg
          

      - name: Push snake animation
        uses: EndBug/add-and-commit@v9
        with:
          message: "Generate contribution snake"
          add: "dist/*.svg"


<!--
**apoorvd06/apoorvd06** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
