# Dependencies

```bash
sudo dnf install neovim ripgrep fzf fd-find tmux unzip gcc make git zsh nodejs golang pnpm maim xdotool stow
```
# Install Tmux TPM
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

# Catpuccin Theme
XFCETerminal :
```bash
mkdir -p $HOME/.local/share/xfce4/terminal/colorschemes
cd  $HOME/.local/share/xfce4/terminal/colorschemes
touch catppuccin-mocha.theme
echo "[Scheme]" >> catppuccin-mocha.theme
echo "Name=Catppuccin-Mocha" >> catppuccin-mocha.theme 
echo "ColorCursor=#f5e0dc" >> catppuccin-mocha.theme
echo "ColorCursorForeground=#11111b" >> catppuccin-mocha.theme
echo "ColorCursorUseDefault=FALSE" >> catppuccin-mocha.theme
echo "ColorForeground=#cdd6f4" >> catppuccin-mocha.theme
echo "ColorBackground=#1e1e2e" >> catppuccin-mocha.theme
echo "ColorSelectionBackground=#585b70" >> catppuccin-mocha.theme
echo "ColorSelection=#cdd6f4" >> catppuccin-mocha.theme
echo "ColorSelectionUseDefault=FALSE" >> catppuccin-mocha.theme
echo "TabActivityColor=#fab387" >> catppuccin-mocha.theme
echo "ColorPalette=#45475a;#f38ba8;#a6e3a1;#f9e2af;#89b4fa;#f5c2e7;#94e2d5;#bac2de;#585b70;#f38ba8;#a6e3a1;#f9e2af;#89b4fa;#f5c2e7;#94e2d5;#a6adc8" >> catppuccin-mocha.theme
```
GTK :
```bash
cd ~/.local/share/themes
# Set the root URL
export ROOT_URL="https://https://github.com/catppuccin/gtk/releases/download"

# Change to the tag you want to download
export RELEASE="v1.0.0"
  
# Change to suite your flavor / accent combination
export FLAVOR="mocha"
export ACCENT="lavender"
curl -LsS "${ROOT_URL}/${RELEASE}/catppuccin-${FLAVOR}-${ACCENT}-standard+default.zip"

# Extract the catppuccin zip file
unzip catppuccin-${FLAVOR}-${ACCENT}-standard+default.zip

# Set the catppuccin theme directory
export THEME_DIR="$HOME/.local/share/themes/catppuccin-${FLAVOR}-${ACCENT}-standard+default"

# Optionally, add support for libadwaita
mkdir -p "${HOME}/.config/gtk-4.0" && 
ln -sf "${THEME_DIR}/gtk-4.0/assets" "${HOME}/.config/gtk-4.0/assets" &&
ln -sf "${THEME_DIR}/gtk-4.0/gtk.css" "${HOME}/.config/gtk-4.0/gtk.css" &&
ln -sf "${THEME_DIR}/gtk-4.0/gtk-dark.css" "${HOME}/.config/gtk-4.0/gtk-dark.css"
```
# Downlaod FiraCode Nerd Font
```bash
mkdir -p $HOME/.fonts/FiraCode/
curl https://github.com/ryanoasis/nerd-fonts/releases/download/v3.2.1/FiraCode.zip -L -o FiraCode.zip
unzip FiraCode.zip -d $HOME/.fonts/FiraCode/
rm FiraCode.zip
```

#Dotfiles + Stow 

```bash
cd
git clone git@github.com:thatmounaim/dotfiles.git
cd $HOME/dotenv
stow .
```
