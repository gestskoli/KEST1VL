## Stillingar á zsh í macos

Búðu til skrána `.zshrc` í heimasvæðinu, með eftirfarandi innihaldi:
```bash
alias ls='ls -G'
alias ll='ls -al'
alias l='ls -lah'
alias la='ls -lAh'
alias ll='ls -lh'
alias lsa='ls -lah'
alias grep='grep --color=auto'
alias fgrep='fgrep --color=auto'
alias egrep='egrep --color=auto'

PS1="%n@%m:%1~: "
```
Vistaðu svo skrána og keyrðu svo eftirfarandi í terminal: `source .zshrc`
