## Bem-vindo! ao meu Github
# Clonando o Repositório git clone https://github.com/Anaak-code/i3.git depois de clonar o meu repositório siga os passos abaixo.
# Depois de ter clonado entre na pasta i3 e dps copie o arquivo config para o ~/.config/i3/config
Agora entra no arquivo config sudo nano ~/.config/i3/config
Procure a linha -> 
```Markdown
# iniciar o terminal
bindsym $mod+Return exec termite
Mude o termite para o seu terminal, caso você não esteja usando o termite, como eu uso termite, eu vou deixar ele. 
Depois disso reinicie seu i3 Mod + Shift + r
```
# Instalando Termite ->
```Markdown
yay -S termite
sudo pacman -S termite
para sistema Debian/Ubuntu ->
git clone --recursive https://github.com/thestinger/termite.git
cd termite && make
Criando pasta do termite e copiando ->
mkdir -p ~/.config/termite
cp /etc/xdg/termite/config ~/.config/termite/config
nano ~/.config/termite/config
pode ir em font = Monospace 9 e coloca o Tamanho da fonte que deseja eu uso em 12, descomente a linha caso tenha #, depois disso salve o arquivo e saia.
```
# Instalando o Rofi e Configurando ->
```Markdown
caso esteja no Arch/Manjaro -> sudo pacman -S rofi
caso esteja Debian/Ubuntu
sudo apt-get update
sudo apt-get install rofi
para abrir ele digite no terminal rofi -show drun!
o arquivo editavel dele fica em cd /usr/share/rofi/themes/
para alterar o tema dele pelo terminal digite -> rofi-theme-selector, escolha um tema e aperte alt + a.
caso queira usar o mesmo tema que eu, clone esse repositório -> git clone https://github.com/davatorium/rofi-themes.git &&  cd rofi-themes/ entre na pasta User Themes, depois  cp flat-orange.rasi /usr/share/rofi/themes/ depois de copiado digite no terminal novamente -> rofi-theme-selector depois de abrir ele procure o tema chamado flat-orange e salve com alt + a.
```

#  Instalando e Configurando a opacidade do compton ->
```Markdown
sudo apt install compton-conf depois disso é só configurar da forma que vocês quer -> para usuários de Debian/Ubuntu
para usuários do Arch -> yay -Syu compton
depois disso copie o arquivo compton do meu repositório e envie ele para ~/.config/compton.conf
agora entre no arquivo nano ~/.config/compton.conf e caso vcs nao queira instalar o termite, vcs tem que alterar o termite pelo terminal de vcs, mas com a inicial em letra Maiúscula.
agora para executar digite -> compton --config ./config/compton.conf

```
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

 # 1 - é preciso clonar o git do polybar-themes. digite github polybar-themes no google.
 # 2 - é preciso clonar o git terroo fonts, só escrever no google github terroo fonts.
se você for coloca as fontes apenas para um usuário ->
```Markdown
cp fonts/ .local/share/fonts/
 caso você queira copiar para todos usuários ->
cp fonts/ /usr/share/fonts/
 Depois de ter copiado a pasta fonts para qualquer um dos diretório, é preciso atualizar o cache. -> fc-cache -fv

 agora é só entrar no diretório clonado, no caso foi o polybar-themes. depois de estar nele escolha um Polybar do seu agrado. agora Você entra na pasta do polybar, copie tudo que está dentro dela para o diretório cp -r * ~/.config/polybar/

Depois disso basta entra na pasta ~/.config/polybar/ e executar o launch.sh

Caso Você queira que ele sempre inicie o sistema com o Polybar, abre o arquivo sudo vim ~/.config/i3/config
agora digite em qualquer linha o seguinte comando -> exec_always --no-startup-id ~/.config/polybar/launch.sh
 toda vez que vc reiniciar o sistema ele vai fica com o polybar.

espero ter ajudado alguém.

Grupo do Discord -> https://discord.gg/FAA4qW2 Comunidade de Programadores.
