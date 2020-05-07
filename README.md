## Bem-vindo! ao meu Github

## Você vai precisa ter o github, caso não tenha abra um terminal e  digite:
# Para Sistema Linux/Debian/Ubuntu
sudo apt-get install git
# Para Sistema Linux/Arch/Manjaro
yay -S pacman git
# Caso não tenha o yay digite pacman.
sudo pacman -S git
# Depois de Instalado o git, continue o tutorial ->
### Customizando o polybar:
Para Customizar o Polybar, Você deve Seguir alguns passos:

 1 - é preciso clonar o git do polybar-themes. digite github polybar-themes.
 2 - é preciso clonar o git terro fonts, só escrever no google github terroo fonts.
 se você for coloca as fontes apenas para um usuário ->
cp fonts/ .local/share/fonts/
 caso você queira copiar para todos usuários ->
cp fonts/ /usr/share/fonts/
 Depois de ter copiado a pasta fonts para qualquer um dos diretório, é preciso atualizar o cache. -> fc-cache -fv

 agora é só entrar no diretório clonado, no caso foi o polybar-themes. depois de estar nele escolha um Polybar do seu agrado. agora Você entra na pasta do polybar, copie tudo que está dentro dela para o diretório cp -r * ~/.config/polybar/

Depois disso basta entra na pasta ~/.config/polybar/ e executar o launch.sh

Caso Você queira que ele sempre inicie o sistema com o Polybar, abre o arquivo sudo vim ~/.config/i3/config
agora digite em qualquer linha o seguinte comando -> exec_always --no-startup-id ~/.config/polybar/launch.sh
 Com isso toda vez que vc reiniciar o sistema ele vai fica com o polybar.

# Lembrando pessoal, eu não mostrei como instalar o Polybar, pois quem vem procurar customização de polybar, ja tem o Polybar não é mesmo.
# espero ter ajudado alguém.

Grupo do Discord -> https://discord.gg/FAA4qW2 Comunidade de Programadores.
