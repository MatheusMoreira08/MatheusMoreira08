<div align="center">
  <img height="150" src="https://media.tenor.com/X8854xxuQ_EAAAAM/destroy-code-mad.gif"  />
</div>

###

<h1 align="center">Olá, 👋 Seja bem-vindo, prazer!!</h1>

###

<h3 align="left">Me chamo Matheus Moreira, sou estudante de programação e amante de tecnologia! Gosto muito da parte de "PO" e "PMO" e tenho um grande interesse na area.</h3>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=MatheusMoreira08&hide_title=false&hide_rank=true&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=aura&locale=en&hide_border=false&order=1" height="155" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=MatheusMoreira08&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=aura&hide_border=false&order=2" height="155" alt="languages graph"  />
</div>

###

<div align="left">
  <img src="https://skillicons.dev/icons?i=js" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=html" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=css" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" height="40" alt="java logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=c" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=vscode" height="40" alt="vscode logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/git/F05032" height="40" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/trello/0052CC" height="40" alt="trello logo"  />
</div>

###

<img align="right" src="https://visitor-badge.laobi.icu/badge?page_id=MatheusMoreira08.MatheusMoreira08&right_color=aquamarine"  />

###

<div align="left">
  <a href="https://www.linkedin.com/in/matheus-moreira-4b876a302" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="52" height="40" alt="linkedin logo"  />
  </a>
  <a href="https://mail.google.com/mail/u/0/#inbox" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/gmail/default.svg" width="52" height="40" alt="gmail logo"  />
  </a>
  <a href="https://www.instagram.com/invites/contact/?utm_source=ig_contact_invite&utm_medium=copy_link&utm_content=9aok25r" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/instagram/default.svg" width="52" height="40" alt="instagram logo"  />
  </a>
</div>

###

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MatheusMoreira08/MatheusMoreira08/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MatheusMoreira08/MatheusMoreira08/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/MatheusMoreira08/MatheusMoreira08/output/pacman-contribution-graph.svg">
</picture>
  name: Generate pacman animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: ${{ github.repository_owner }}


      - name: push pacman-contribution-graph.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

###


