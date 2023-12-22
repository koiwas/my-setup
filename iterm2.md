# iterm2

iterm2をダウンロード<br>
https://iterm2.com/

.zshrcを開いて編集モードを開始（i）

```
vi .zshrc
```

以下を貼り付けて編集モードを終了(esc)

```
export TERM=xterm-256color

autoload -Uz vcs_info
setopt prompt_subst
zstyle ':vcs_info:git:*' check-for-changes true
zstyle ':vcs_info:git:*' stagedstr "%F{magenta}!"
zstyle ':vcs_info:git:*' unstagedstr "%F{yellow}+"
zstyle ':vcs_info:*' formats "%F{cyan}%c%u[%b]%f"
zstyle ':vcs_info:*' actionformats '[%b|%a]'
precmd () { vcs_info }

PROMPT='%B%F{red}%m%f%b:%F{green}%~%f%F{cyan}$vcs_info_msg_0_%f
$ '
```

保存(:wq)して適用

```
source .zshrc
```
