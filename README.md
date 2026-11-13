# 🚀 Cyfrinup  

**The all-in-one security toolkit** for downloading Command Line tools from Cyfrin.

### ✅ Supported Platforms  
- Linux  
- macOS  
- WSL  

⚠️ Windows native users cannot use Cyfrinup and should manually download supported tools from their respective repositories.  

## 🛠 Installation  

Run the following command to install Cyfrinup:  

```bash
curl -L https://raw.githubusercontent.com/Cyfrin/up/main/install | bash
```

> NOTE: If you have previously installed Cyfrinup from [Aderyn](https://github.com/Cyfrin/aderyn)'s repository, you do not have to install it again.

## 📦 Tools Included  

| Tool      | Description | Supported Platforms |
|-----------|------------|--------------------|
| [Safe-Hash](https://github.com/Cyfrin/safe-hash-rs) | Safe Wallet Tx Verificaton tool | Linux, macOS, WSL, Windows (Intel) |


## Aderyn retirement

Aderyn has been retired and is no longer maintained. Cyfrinup no longer installs or updates it. Running `cyfrinup` installs Safe-Hash only; `CYFRINUP_ONLY_INSTALL=aderyn cyfrinup` prints a retirement notice and exits with an error.

Existing Aderyn installations are not removed automatically. For a Cyfrinup installation using the default paths, remove its binaries and install receipt with the commands below. If you used a custom installation directory, check `command -v aderyn` and `command -v aderyn-update` and adjust the binary paths first.

```bash
rm -f "${CARGO_HOME:-$HOME/.cargo}/bin/aderyn" "${CARGO_HOME:-$HOME/.cargo}/bin/aderyn-update"
rm -f "$HOME/.cyfrin/bin/aderyn"
rm -f "${XDG_CONFIG_HOME:-$HOME/.config}/aderyn/aderyn-receipt.json"
```

If you installed it another way (Homebrew, npm, `cargo install`), uninstall it with that package manager instead.

## 🚀 Usage  

After installation, run the following command to download all available tools:  
```bash
cyfrinup
```  
This will fetch and install all supported tools for your platform. 🚀
