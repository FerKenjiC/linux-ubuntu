<h1> Códigos do Ubuntu </h1>

<h3>Observação:</h3>
  Comando <strong>sudo</strong> concede privilégio de admistrador <br>
  Comando <strong>apt:</strong> gerenciador de pacotes 

- <strong>Ctrl + Alt + T </strong> <br>
  Abre o Terminal.
- <strong>sudo rebbo </strong> <br>
  Reinicia o Ubuntu.
- <strong>sudo apt update </strong> <br>
  Baixa as atualizações para o Ububtu.
- <strong>sudo apt upgrade </strong> <br>
  Instala as atualizações.
- <strong>sudo update && sudo upgrade </strong> <br>
  Faz as duas coisas de uma vez.
- <strong>sudo apt install build-essential dkms linux-heafers-$(uname -r)</strong> <br>
  Instala: install build-essential: ferramenta para compilar código-fonte
- <strong>dkms:</strong> recompilador de aplicações para compatibilidade com Kernel do convidado (guest)
- <strong>cd /media/$USER/VBox_Gas_7.0.6</strong> <br>
  Caminha até o diretório onde está o dispositivo para instalar recursos adicionais de convidado. <strong>$USER</strong> é uma <br> variável de ambiente que rederencia o valor do usuário que está logado (nome de usuário). 
- <strong>sudo ./VBoxLinuxAdditions.run</strong> <br>
  Executa o aplicativo deponível no diretório que acessou e instala os recursos.
- <strong>lsmod | grep vbox</strong> <br>
  - <strong>lsmod:</strong> Listar módulos carregados no Kernel.
  - <strong>grep:</strong> funciona como um filtro para pesquisar apenas as linhas que contenham o texto que deseja pesquisar (nesse caso, vbox).
  - <strong>vbox:</strong> prefixo que inicia normalmente os nomes dos módulos do VirtualBox.
