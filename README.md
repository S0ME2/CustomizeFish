# 🪄 Install Oh My Posh on Linux

Oh My Posh is a prompt theme engine for any shell, designed to make your terminal look stunning and informative.  
This guide walks you through installing and configuring **Oh My Posh** on **Linux** with the **Fish shell**.

---

## ⚙️ Step 1: Download and Install Oh My Posh

Use the following commands to download the latest Linux binary and make it executable:

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```

This installs `oh-my-posh` globally so it can be used from any shell.

---

## 🎨 Step 2: Install Fonts

Oh My Posh themes use **Nerd Fonts** to display icons correctly.  
Run the following command to install a compatible font:

```bash
oh-my-posh font install
```

Then open your terminal’s **Appearance Settings** and select the newly installed Nerd Font as your terminal font.

---

## 🧩 Step 3: Choose a Theme

List available themes by running:

```bash
ls ~/.poshthemes
```

Each `.omp.json` file in that directory represents a theme.

---

## 📝 Step 4: Configure Fish Shell

Edit your Fish configuration file located at:

```bash
~/.config/fish/config.fish
```

Add (or adjust) the Oh My Posh initialization line to include your chosen theme configuration.  
For example:

```bash
oh-my-posh init fish --config ~/.poshthemes/jandedobbeleer.omp.json | source
```

💡 Replace `jandedobbeleer.omp.json` with the theme you want to use.

---

## 🔄 Step 5: Apply Changes

Reload your Fish configuration to apply the new prompt:

```bash
. ~/.config/fish/config.fish
```

---

## 👀 Step 6: Explore Themes

To preview available themes visually, visit:  
👉 [https://ohmyposh.dev/docs/themes](https://ohmyposh.dev/docs/themes)

---

## ✅ Done!

You now have **Oh My Posh** up and running on Linux 🎉  
Enjoy a beautiful and informative terminal experience!
