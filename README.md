# GINES Desktop — instaladores

Instaladores do app desktop do GINES (Linux e macOS), gerados pelo pipeline do repositório `gines-client`. Os arquivos ficam em
[Releases](https://github.com/gines-ai/gines-desktop-releases/releases); cada versão traz o `sha256` de cada pacote.

## Linux (Ubuntu, Debian)

```sh
sudo apt install ./gines-<versão>-amd64.deb
```

Instala em `/opt/GINES`, cria o comando `gines` e, no Ubuntu 24.04 ou mais novo, o perfil AppArmor
`/etc/apparmor.d/gines`, que permite ao app rodar com o sandbox do sistema. O app não roda sem sandbox.

Remover: `sudo apt remove gines` (os dados ficam em `~/.config/GINES`).

## Linux (Fedora, RHEL, openSUSE)

```sh
sudo dnf install ./gines-<versão>-x86_64.rpm       # openSUSE: sudo zypper install ./gines-<versão>-x86_64.rpm
```

Instala em `/opt/GINES` e cria o comando `gines`. As próximas versões chegam sozinhas (Ajustes → Versão; o sistema
pede a senha de administrador para instalar).

Remover: `sudo dnf remove gines` (ou `sudo zypper remove gines`; os dados ficam em `~/.config/GINES`).

## macOS 12 ou mais novo

Baixe `gines-<versão>-arm64.dmg` (Apple Silicon, M1 ou mais novo) ou `gines-<versão>-x64.dmg` (Intel), abra e
arraste o GINES para **Aplicativos**. O app é assinado (Developer ID) e notarizado pela Apple: abre sem aviso de
desenvolvedor não identificado.

As próximas versões chegam sozinhas (Ajustes → Versão) quando o GINES é aberto pela pasta Aplicativos; aberto
direto do `.dmg`, ele não tem onde se atualizar. Os `.zip` de cada versão são os que o atualizador baixa.

Remover: arraste o GINES de Aplicativos para o Lixo (os dados ficam em `~/Library/Application Support/GINES`).
