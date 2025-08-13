-+<h1>Códigos do Ubuntu</h1>

<h3>Observação:</h3>
  Comando <strong>sudo</strong> concede privilégio de admistrador <br>
  Comando <strong>apt:</strong> gerenciador de pacotes 

---
- <strong>Ctrl + Alt + T </strong> <br>
  Abre o Terminal.
- <strong>sudo rebbo </strong> <br>
  Reinicia o Ubuntu.
---
- <strong>sudo apt update </strong> <br>
  Baixa as atualizações para o Ububtu.
- <strong>sudo apt upgrade </strong> <br>
  Instala as atualizações.
- <strong>sudo update && sudo upgrade </strong> <br>
  Faz as duas coisas de uma vez.
---
<strong>Comandos para Redimencionar a tela do Ubunto</strong>
---
- <strong>sudo apt install build-essential dkms linux-heafers-$(uname -r)</strong> <br>
  Instala: install build-essential: ferramenta para compilar código-fonte
- <strong>dkms:</strong> recompilador de aplicações para compatibilidade com Kernel do convidado (guest)
- <strong>cd /media/$USER/VBox_Gas_7.0.6</strong> <br>
  Caminha até o diretório onde está o dispositivo para instalar recursos adicionais de convidado. <strong>$USER</strong> é uma <br> variável de ambiente que rederencia o valor do usuário que está logado (nome de usuário). 
- <strong>sudo ./VBoxLinuxAdditions.run</strong> <br>
  Executa o aplicativo deponível no diretório que acessou e instala os recursos.
--- 
- <strong>lsmod | grep vbox</strong> <br>
  - <strong>lsmod:</strong> Listar módulos carregados no Kernel.
  - <strong>grep:</strong> funciona como um filtro para pesquisar apenas as linhas que contenham o texto que deseja pesquisar (nesse caso, vbox).
  - <strong>vbox:</strong> prefixo que inicia normalmente os nomes dos módulos do VirtualBox.
---
<strong>Connfiguração da VM (host)</strong>
---
<ul>
  <li>Criação de uma nova pasta na máquina física <strong>VirtualBox-PastaCompartilhada</strong></li>
  <li>Criamos documentos de texto com o nome arquivo_teste_host.</li>
  <li>Foi escrito dentro deste arquivo a mensagem "Este é um teste para pasta compartilhada entre host (máquina física) e guest (virtual)".</li>
</ul>

---
<strong>Connfiguração da VM (guest)</strong>
---
- Virtual BOx - COnfigurações - Pasta Compartilhada - Adicionar - Selecionar pasta no disco local.
  - Iniciar Ubunto.
  - Acessar Terminal
- <strong>sudo adduser $USER vboxsf</strong> <br>
  - Adiciona o usuário no grupo vboxsf após isto, dar sudo reboot para reiniciar. <br>
- <strong>cd /media/sf_VirtualBox-PastaCOmpartilhada</strong> <br>
  - Acessa o diretório da pasta compartilhada.
- <strong>cd ../</strong> <br>
  - Voltar no diretório, na pasta anterior
- <strong>ls</strong> <br>
  - Lista os arquivos na pasta.
- <strong>echo "Mensagem que você quer adicionar" > (nome do arquivo "arquivo_teste" e não esquecer da extensão ".txt")</strong> <br>
  - Cria uma arquivo na pasta compartilhada.
- <strong>cat + "nome do arquivo de texto"</strong> <br>
  - Permite ler o que está no arquivo de texto.

- Após isso utilizamos um arquivo padrão do Ubunto para abrir o arquivo e edita-lo.
  - nano (nome do arquivo) = Usar Ctrl + os guias que tem no próprio nano.
- Foi instalado um segundo aplicativo padrão do Ubunto para abrir o arquivo e edita-lo
  - digite "vim" sem estar no diretório da pasta compartilhada e aparecerá os comandos de instalação.
---
- Dentro do diretírio: cd /media/sf_VirtualBox_PastaCOmpartilhada
- <strong>ls -l</strong> <br>
  - lista o arquivos com mais especificações, como data e hora da última alteração feita no arquivo. <br>
  ex:
    - <strong>drwxr-xr-x 2 root alunos 4096 ago 11 21:29 pasta_alunos</strong>
    - <strong>drwxr-x--- 2 senac senac 4096 ago 11 20:24 pasta_alunos</strong>
  - d = diretório.
  - r = ler.
  - w = gravar dados.
  - x = executar.
  - "-" = sem permissão.
  - root = é o usuário proprietário.
  - "alunos" = é o grupo proprietário.
  - 4096 = é o tamanho do arquivo.
- <strong>sudo addgroup (nome) </strong>.
  - cria um grupo.
- Adicionar um usuário a um grupo no SO.
  - <strong>sudo adduser $USER (nome do grupo) </strong> (Ubunto/ Debian Desktop)
  - <strong>sudo usermod -aG (nome do usuário) nome_do_grupo1 nome _do_grupo2</strong> <br>
      Utilizar essa opção pois ele adiciona o usuário ao novo grupo, mas mantem o mesmo nos grupos que ele já integrava.
  - <strong>sudo usermod -aG nome_do_grupo1 nome_do_grupo2 $USER</strong>
- <strong>sudo mkdir home/(nome do diretório)</strong>
  - Para criar um novo diretório
- <strong>sudo chown :nome_do_grupo nome_da_pasta</strong> <br>
  - Para mudar o grupo proprietário de um diretório
- 
