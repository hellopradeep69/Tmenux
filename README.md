## tmenux / tmux-wander

---

1. what is tmenux ?

- tmenux is a succesor of tmenu

2. how is it different from tmenu ?

- templates feature is removed cuz i never used it instead we have like [Home]
- session from directory is now not a submenu . its build in
- rest are somewhat same

---

### Installation

```bash
mkdir -p ~/.local/bin
curl -L https://raw.githubusercontent.com/hellopradeep69/Tmenux/main/tmenux.sh -o ~/.local/bin/tmenux.sh
```

- give permisson to the file .

```bash
chmod +x ~/.local/bin/tmenu.sh
```

---

#### keybind (shortcuts)

- add in your .tmux.conf

```.tmux.conf
bind-key f run-shell "tmux neww -n 'Tmenu' ~/.local/bin/tmenux.sh"
```

- prefix + f opens the tmenu so you dont have to type it every time you want to open it
- prefix default it ctrl + b. [weird]

---
