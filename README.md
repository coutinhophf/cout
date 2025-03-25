# cout
Trabalho Inicial
name: Deploy para GitHub Pages
on: 
  push:
       branches:
       - main # Executa quando há mudanças na brach principal 
permissions: 
  contentes: write 
  pages: write
  id-token: write 

jobes:
  deploy: 
    runs-on: ubuntu-latest 

    steps: 
      -name: Checkout do repositório 
       uses: actions/checkout@v4

      -name: Configurar GitHub Pages
       users: action/configure-pages@v5

      -name: Criar artefato para deploy 
       users: actions/upload-pages-artifact@v3 # Pode tentar também @v2 se funcionar
       with: 
         path: .

       -name: Publicar no GitHub Pages
        users: actions/deploy-pages@v4
  :   
       
