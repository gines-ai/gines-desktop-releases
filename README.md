# GINES Desktop — instaladores

Instaladores do app desktop do GINES, gerados pelo pipeline do repositório `gines-client`. Os arquivos ficam em
[Releases](https://github.com/gines-ai/gines-desktop-releases/releases); cada versão traz o `sha256` do pacote.

## Linux (Ubuntu/Debian)

```sh
sudo apt install ./gines-<versão>-amd64.deb
```

Instala em `/opt/GINES`, cria o comando `gines` e, no Ubuntu 24.04 ou mais novo, o perfil AppArmor
`/etc/apparmor.d/gines`, que permite ao app rodar com o sandbox do sistema. O app não roda sem sandbox.

Remover: `sudo apt remove gines` (os dados ficam em `~/.config/GINES`).
