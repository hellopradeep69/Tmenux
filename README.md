## tmenux / tmux-wander

1. what is tmenux ?

- tmenux is a successor of [Tmenu](https://github.com/hellopradeep69/Tmenu.git) .
- it works the same but with lil change mention below
- feel free to try/checkout Tmenu too .

2. how is it different from tmenu ?

- templates feature is removed cuz i never used it instead we have like [Home]
- session from directory is now not a submenu , its build in (just like Tmux-sessionzer)
- delete feature still exist , incase you wanna delete a bunch of tmux server in one go .
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

### Customizability

1. Exclude Directory

- You can exclude dir that you dont want to include in the script .
- Default is given below . you can add more in the script .
- Exclude dir section is under "Exclude Directories Mention"

```bash
EXCLUDE_DIRS=(~/.cache ~/.rustup ~/.npm ~/.zen ~/.linuxmint ~/.icons ~/Desktop ~/.cargo ~/.mozilla ~/.themes)
```

2. Session Overview

- You can change the existing session Overview in script
- Predefined variable are available in the script
- Session Overview section under "FORMAT SESSION"
- - Default

```bash
    printf "%-20s [%d pane(s)] %s %s\n" "$name" "$total_panes" "$marker" "$smarker"
```

- Example

1. simple

```bash
    echo "$name (created: $date_str) $marker $smarker"
```

2. with date and marker like attatched and spilt-panes

```bash
    printf "%-20s %-22s %s %s\n" "$name" "(created: $date_str)" "$marker" "$smarker"
```

or

```bash
    printf "%-13s %-28s %s %s\n" "$name" "(created: $date_str)" "$marker" "$smarker"
```

---

#### keybind (shortcuts)

- add in your .tmux.conf

```.tmux.conf
bind-key f run-shell "tmux neww -n 'Tmenu' ~/.local/bin/tmenux.sh"
```

- prefix + f opens the tmenu so you dont have to type it every time you want to open it
- prefix default is ctrl + b. [weird]

---
