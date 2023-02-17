### 👋 Olá! Eu sou a Angela Guacaran

- 💻 Estou trabalhando como desenvolvedora web júnior
- 🌱 Estudando Javascript, Figma
- 📧 Contate-me no email: angelaguacaran@gmail.com

- 😄 Pronouns: Ela/dela 

<div alinear="center">
  <a href="https://github.com/Angelag-39">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Angelag-39&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Angelag-39&layout=compact&langs_count=7&theme=dracula"/> 
</div>


  <div>
      <a href="https://www.linkedin.com/in/angela-daniela-guacaran-regalado-17805a1b8" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  </div>

</div>
 
 <div style="display:inline_block"><br>
 <img align="center" alt="Angela-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Angela-Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Angela-React" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
    <img align="center" alt="Angela-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Angela-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Angela-PHP" height="30" width="40" src="https://user-images.githubusercontent.com/102700392/217883735-38edf370-bed5-4e1b-8cd9-c3b673fa7b6b.png">
 <img align="center" alt="Angela-Java" heigth="30" width="40" src="https://cdn-icons-png.flaticon.com/512/5968/5968282.png">
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
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
