### Hi there 👋 me chamo <-- João Araújo -->

<!--
**slkjao/slkjao** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.


- 🔭 Procurando primeiro emprego na área de ti
- 🌱 Estou aprendendo Spring
- 👨‍🎓 3o Período em Análise e Desenvolvimento de Sistemas - Newton Paiva (EAD) (Curso Trancado)
- 📫 Contato por email: joaovaraujoc@gmail.com

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
          github_user_name: slkjao
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
