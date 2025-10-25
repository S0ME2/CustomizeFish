# 🪄 Make Your Linux Terminal Look Amazing  
### Using Fish Shell + Oh My Posh

While the default Linux terminal prompt can be a bit plain, you can easily transform it into something **beautiful and informative**.  
This documentation will guide you through setting up the **Fish shell** with **Oh My Posh** to create a powerful, visually appealing, and highly personalized terminal experience.

---

## 🐟 Introduction

**Fish shell** (Friendly Interactive Shell) is a user-friendly shell with:

- 🧠 Autosuggestions  
- 🎨 Syntax highlighting  
- ⚙️ Easy scripting  

It’s powerful, intuitive, and perfect for both beginners and advanced users.

**Oh My Posh** is a **universal prompt theme engine** that works with any shell.  
It provides stunning, customizable prompts showing details like Git status, system info, battery, and more.

After following this guide, you’ll have a **fully functional, beautiful Linux terminal** that reflects your style and improves productivity.  
Get ready to rock your shell—with some handy aliases too!

---

## ⚙️ Step 1: Install Fish Shell

### 🧩 Ubuntu / Debian / Linux Mint

```bash
sudo apt install fish -y
```

### 🧩 Fedora

```bash
sudo dnf install fish -y
```

### 🧩 Arch Linux / Manjaro Linux

```bash
sudo pamac -S fish --noconfirm
```

---

## 🐚 Step 2: Change Default Shell to Fish

To make Fish your default shell:

```bash
chsh -s /usr/bin/fish
```

Then start Fish manually:

```bash
fish
```

---

## ⚙️ Step 3: Install Oh My Posh

Download and install the latest Linux binary:

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```

This installs **Oh My Posh** globally so it can be used from any shell.

---

## 🎨 Step 4: Download and Install Fonts

Oh My Posh themes require **Nerd Fonts** to display icons properly.

### Create fonts directory:

```bash
mkdir -p $HOME/.local/share/fonts
```

### Download FiraCode Nerd Font:

```bash
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/FiraCode.zip -O $HOME/Downloads/firacode.zip
unzip $HOME/Downloads/firacode.zip -d $HOME/.local/share/fonts
```

### Update font cache:

```bash
fc-cache -f -v
```

---

## 🧠 Step 5: Set Terminal Font

Change your system **Monospace Text Font** to **FiraCode Nerd Font Mono**.

If you’re using GNOME, install **GNOME Tweaks**:

### Ubuntu / Debian / Linux Mint

```bash
sudo apt install gnome-tweaks -y
```

### Fedora

```bash
sudo dnf install gnome-tweaks -y
```

### Arch / Manjaro

```bash
sudo pamac -S gnome-tweaks --noconfirm
```

Then open **GNOME Tweaks → Fonts → Monospace Text** and select *FiraCode Nerd Font Mono*.

---

## 🧩 Step 6: Download and Install Oh My Posh Themes

```bash
mkdir ~/.poshthemes
wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/themes.zip -O ~/.poshthemes/themes.zip
unzip ~/.poshthemes/themes.zip -d ~/.poshthemes
chmod u+rw ~/.poshthemes/*.json
rm ~/.poshthemes/themes.zip
```

Each `.omp.json` file inside this directory is a theme configuration.

---

## 📝 Step 7: Configure Fish Shell

Edit your Fish configuration file:

### Open with gedit:

```bash
gedit $HOME/.config/fish/config.fish
```

### Or nano:

```bash
nano $HOME/.config/fish/config.fish
```

Add the following line at the bottom:

```bash
oh-my-posh init fish --config $HOME/.poshthemes/montys.omp.json | source
```

💡 Replace `montys.omp.json` with your desired theme.

---

## 🌈 Step 8: Change Terminal Color Scheme

To enhance visuals, change your terminal color scheme.

Example:  
Choose **Everforest Dark Hard** (option 69 in GNOME Terminal preferences).

---

## 🔄 Step 9: Apply and Verify

Reload your Fish configuration:

```bash
. ~/.config/fish/config.fish
```

If your GNOME Terminal doesn’t load Fish as the default shell, log out and back in again.  
After that, your terminal will start with Fish automatically.

---

## 👀 Step 10: Explore Themes

List all installed themes:

```bash
ls ~/.poshthemes
```

Preview all official Oh My Posh themes at:  
👉 [https://ohmyposh.dev/docs/themes](https://ohmyposh.dev/docs/themes)

---

## ✅ Done!

You now have **Fish shell** and **Oh My Posh** fully configured on Linux 🎉  
Enjoy your **beautiful, efficient, and informative terminal**.

---

## 📚 References

- [Oh My Posh Official Docs](https://ohmyposh.dev/docs)  
- [Fish Shell Official Docs](https://fishshell.com/docs/current/)  
- [Nerd Fonts Repository](https://github.com/ryanoasis/nerd-fonts)
