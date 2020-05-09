## Bem-vindo! ao meu Github
# Resultado final ->
![Screenshot from 2020-05-07 21-12-10](https://user-images.githubusercontent.com/64982678/81356422-8693e900-90a7-11ea-862f-807453d4e11b.png)

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
# Scripts -> tty-clock e ncmpcpp. tty-clock apenas pode ser clonado ou usando o yay ou trizen no arch, ja o ncmpcpp pode baixar atraves do repositorio padrao, usando tanto pacman quanto apt-get install ncmpcpp.
```Markdown
# Instalando ncmpcpp ->
sudo apt-get install ncmpcpp
sudo apt-get install mpd
sudo pacman -S ncmpcpp
sudo pacman -S mpd 
mpd é um servidor de reprodução de música.

<h3>criando a pasta do ncmpcpp e mpd e configurando</h3>
1 - mkdir .mpd .ncmpcpp
2 - cd .ncmpcpp
3 - touch config, depois de criar o arquivo config dentro do ncmpcpp copie o arquivo do repositorio dentro da pasta ncmpcpp com o nome config para ~/.ncmpcpp depois saia e vai pra pasta .mpd
4 - cd .mpd/ 
5 - crie o arquivo chamado mpd.conf dentro da pasta .mpd/
6 - depois copie o arquivo do repositorio na pasta ncmpcpp/ com o nome do arquivo mpd.conf para ~/.mpd
7 - agora de um cat mpd.conf para ver se ta tudo certo.
8 - crie 3 arquivos com o comando touch mpd.db mpd.log mpd.pid dentro da pasta .mpd.
9 - agora vcs vai abrir com o gedit o arquivo mpd.conf depois de aberto vcs vai mudar o seguinte ->
music_directory "/root/Music"
playlist_directory "/root/Music"
em /root/Music e /root/Music vcs vai alterar para o diretorio onde se encontra a playlist de Musicas de vcs.
depois de fazer isso salve o arquivo e saia, entre na pasta .ncmpcpp/ e edite o arquivo novamente com o gedit -> gedit config
e altere para o diretorio onde se encontra a playlist de vcs.
music_directory "/root/Music"
playlist_directory "/root/Music"
depois de fazer isso tudo, salve e saia agora da mpd no terminal, depois de da mpd execute o comando ncmpcpp, e sua imagem deve está igual a minha ->
```
![Screenshot from 2020-05-07 21-45-40](https://user-images.githubusercontent.com/64982678/81358197-353a2880-90ac-11ea-8605-5f2caf9147d8.png)
<h3> com as teclas 1 2 3 4 5 6 7 8 vc navega pelo ncmpcpp.</h3>
<h3> na tecla 2 fica suas músicas, a tecla 1 é onde sua playlist está e as outras teclas vc vão vendo.</h3>
<h3> caso você não coloco correto o diretório da sua pasta de playlist de músicas não vai aparecer nenhuma música.</h3>
<h3>caso isso aconteça você deve mudar o diretório e colocar corretamente!</h3>

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
## Você vai precisa ter o git, caso não tenha abra um terminal e  digite:
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
se você for colocar as fontes apenas para um usuário ->
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
