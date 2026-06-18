## Ola sou o Miguel de Souza Rodrigues 👋


- 🔭 Aspirante de Engenharia de Software na UniCesumar
- 🌱 Estudando Inteligencia Artificial
- 💬 contate-me no email:miguelsouzarodrigues50@gmail.com

-->

  
  
 
<div> 
  <a href="https://instagram.com/_souzzxx" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:miguelsouzarodrigues50@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/miguel-rodrigues-14a29a384" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
</div>

<div>
  <a href="https://github.com/MiguelRodrigues">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=MiguelRodrigues&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MiguelRodrigues&layout=compact&langs_count=16&theme=dark"/>
</div>

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Miguel-Rodrigues
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
