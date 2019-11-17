<h1 align="center">
Navegue de forma confortavel pelos diretorios 
</h1>

---------------------------

<h1 align="center">Breve instrodução</h1>

Os usuários do Linux geralmente precisam usar um comando repetidamente. Digitar ou copiar o mesmo comando repetidamente reduz sua produtividade e o distrai do que você está realmente fazendo.

Você pode economizar algum tempo criando aliases para os comandos mais usados. Os aliases são como atalhos personalizados usados para representar um comando (ou conjunto de comandos) executado com ou sem opções personalizadas. Provavelmente, você já está usando aliases no seu sistema Linux.

* sempre que tiver que fazer o mesmo comando por varias veses é bom criar aliases.
* para mais informações acesse o [site] (https://tiagotgv.github.io/aliases/)

```
$ alias docs="cd ~/Documentos"
```

------------------------------


# Navegação mais fácil
```
$ alias ..="cd .."

$ alias ...="cd ../.."

$ alias ....="cd ../../.."

$ alias .....="cd ../../../.."

$ alias ~="cd ~" # `cd` is probably faster to type though

$ alias -- -="cd -"
alias cat=ccat
```

# Atalhos

```
$ alias docs="cd ~/Documentos"

$ alias dl="cd ~/Downloads"

$ alias dt="cd ~/Desktop"

$ alias sb="cd ~/sandbox"

$ alias g="git"

$ alias h="history"

$ alias dir='ls'

$ alias python='python3'

$ alias @gv='gvim'

$ alias @v='vim'

$ alias @p='python3'

$ alias @ip='ipython'

$ alias @da='django-admin.py'

$ alias @pm='python manage.py'

$ alias @wo='workon'

$ alias @de='deactivate'

$ alias @ct='tdaemon --custom-args="--verbosity=2 --rednose --force-color"'

$ alias @ctd='tdaemon --test-program=django --custom-args="--verbosity=2 --rednose --force-color"'

$ alias open='nautilus'

$ alias r='rails'

$ alias gi='gem install'

$ alias ack='ack-grep'

$ alias gst='git status'

$ alias gch='git checkout'

$ alias gb='git branch'

$ alias gco='git commit'

$ alias gdf='git diff'

$ alias ls='ls -liash --color=auto'

$ alias vbox='vagrant box'

$ alias vinit='vagrant init'

$ alias vup='vagrant up'

$ alias vssh='vagrant ssh'

$ alias vreload='vagrant reload'

$ alias vhalt='vagrant halt'

$ alias vsuspend='vagrant suspend'

$ alias vresume='vagrant resume'

$ alias vdestroy='vagrant destroy'

$ alias vprovision='vagrant provision'

$ alias vstatus='vagrant status'

$ alias weechat='weechat-curses irc://irc.freenode.net'

$ alias rspec='rspec --color'

$ alias apt-get='sudo apt-get'
```

# Aliases de comando DOCKER  

```
$ alias docker='docker'

$ alias dockr='docker run'

$ alias dockps='docker ps'

$ alias dockrm='docker rm'

$ alias docki='docker images'

$ alias dockrmi='docker rmi'


# Liste todos os arquivos coloridos em formato longo

$ alias l='ls -l --color'

$ alias lisah='ls -lisah --color'


```

# lista todos os arquivos coloridos em formato longo, incluindo arquivos de ponto

```
$ alias la='ls -la --color'
```


## Listar apenas diretórios

```
$ alias lsd='ls -l --color | grep "^d"'
```


# Endereços IP
```
$ alias ip="dig +short myip.opendns.com @resolver1.opendns.com"

$ alias localip="sudo ifconfig getifaddr wlan0"

$ alias ips="sudo ifconfig -a | grep -o 'inet6\? \(\([0-9]\+\.[0-9]\+\.[0-9]\+\.[0-9]\+\)\|[a-fA-F0-9:]\+\)' | sed -e 
's/inet6* //'"
```


# Pesquisas WHOIS aprimoradas

```
$ alias whois="whois -h whois-servers.net"
```


# Liberar cache do serviço de diretório

```
$ alias flush="dscacheutil -flushcache && killall -HUP mDNSResponder"
```


# View HTTP traffic

```
$ alias sniff="sudo grep -d 'wlan0' -t '^(GET|POST) ' 'tcp and port 80'"

$ alias httpdump="sudo tcpdump -i wlan0 -n -s 0 -w - | grep -a -o -E \"Host\: .*|GET \/.*\""
```


# Alguns aliases úteis do nmap para modos de verificação


# As opções do Nmap são:

-sS - Varredura TCP SYN

-v - detalhado

-T1 - tempo da verificação. As opções são paranóicas (0), sorrateiras (1), educadas (2), normais (3), agressivas (4) e 
insanas (5)

-sF - Varredura FIN (pode se infiltrar através de firewalls não controláveis)

-PE - Sonda de descoberta de eco ICMP

-PP - probe descoberta de carimbo de data e hora

-PY - Ping inicial do SCTP

-g - usa o número fornecido como porta de origem

-A - ativa a detecção do SO, detecção de versão, varredura de script e traceroute (agressivo)

-O - ativar a detecção do SO

-sA - Varredura de confirmação de TCP

-F - verificação rápida

--script = vuln - também acessa vulnerabilidades no destino

```
$ alias nmap_open_ports = " nmap --open "

$ alias nmap_list_interfaces = " nmap --iflist "

$ alias nmap_slow = " sudo nmap -sS -v -T1 "

$ alias nmap_fin = " sudo nmap -sF -v "

$ alias nmap_full = " sudo nmap -sS -T4 -PE -PP -PS80.443 -PY -g 53 -A -p1-65535 -v "

$ alias nmap_check_for_firewall = " sudo nmap -sA -p1-65535 -v -T4 "

$ alias nmap_ping_through_firewall = " nmap -PS -PA "

$ alias nmap_fast = " nmap -F -T5 --version-light --top-ports 300 "

$ alias nmap_detect_versions = " sudo nmap -sV -p1-65535 -O --osscan-guess -T4 -Pn "

$ alias nmap_check_for_vulns = " nmap --script = vuln "

$ alias nmap_full_udp = " sudo nmap -sS -sU -T4 -A -v -PE -PS22,25,80 -PA21,23,80,443,3389 "

$ alias nmap_traceroute = " sudo nmap -sP -PE -PS22,25,80 -PA21,23,80,3389 -PU -PO --traceroute "

$ alias nmap_full_with_scripts = " sudo nmap -sS -sU -T4 -A -v -PE -PP -PS21,22,23,25,80,113.31339 -PA80.113.443.10042 -PO --
script all " 

$ alias nmap_web_safe_osscan = " sudo nmap -p 80.443 -O -v --osscan-guess --fuzzy "
```



* Caso queira remover um ou todos os aliases execute os comandos abaixo:

```

$ unalias alias_name [remove um alias]



$ unalias -a  [remove todos os alias]

```

#### Desintalar aliases

```
$ unalias ls

$ alias ls='ls -l --color'

$ alias ark='file-roller
```

```
$ unalias ls

$ alias ls='ls -l --color'

$ alias ark='file-roller
```
