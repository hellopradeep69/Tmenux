## tmenux / tmux-wander

1. what is tmenux ?

- tmenux is a successor of [Tmenu](https://github.com/hellopradeep69/Tmenu.git) .
- it works the same but with lil different change mention below
- feel free to try/checkout Tmenu too .

2. how is it different from tmenu ?

- templates feature is removed cuz i never used it instead we have like [Home]
- session from directory is now not a submenu , its build in (just like Tmux-sessionzer)
- delete feature still , if exist you wanna delete a bunch of tmux in one go .
- rest are somewhat same

---

### Features

- Existing tmux server visible
- Home - Opens a tmux server in your home directory
- Delete - it Deletes .
- Exclude unwanted directory [ Totally Customizeable]
- Attatched tmux indicator - [attached]
- Zoomed / split tmux indicator - [Z]
- Tmux-sessionzer inspired stuff

---

### Requirement

- fzf
- tmux
- curl
- linux os/ macos [cuz window sucks]

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
