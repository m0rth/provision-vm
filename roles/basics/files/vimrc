ZSH=~/.oh-my-zsh
# Lines configured by zsh-newuser-install
HISTFILE=~/.histfile
HISTSIZE=10000
SAVEHIST=10000
DISABLE_AUTO_UPDATE="true"
setopt appendhistory autocd extendedglob
bindkey -e

ZSH_THEME="agnoster"
ENABLE_CORRECTION="true"
COMPLETION_WAITING_DOTS="true"

export VISUAL=vim
export EDITOR="$VISUAL"

autoload -Uz compinit
compinit
autoload -U colors && colors

# aliases
alias grep='grep --color=auto'
alias mkdir='mkdir -p -v'
alias df='df -h'
alias du='du -c -h'

# privileged access
if [ $UID -ne 0 ]; then
  alias sudo='sudo '
  alias scat='sudo cat'
  alias sn='sudo nano'
  alias root='sudo -s'
  alias reboot='sudo reboot'
fi

# ls
alias ls='ls -hF --color=auto'
alias lx='ll -BX'                   # sort by extension
alias lz='ll -rS'                   # sort by size
alias lm='la | more'

source $ZSH/oh-my-zsh.sh
