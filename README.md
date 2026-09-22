# mgd-pkg

Estudo de empacotamento e distribuição de assets binários grandes com atualização incremental.

Projeto pessoal pra experimentar como distribuir pacotes de arquivos grandes pra aplicações
desktop de forma eficiente:

- **Sincronização por manifest** — um `manifest.json` lista cada asset com tamanho e hash
  SHA-256, mais uma versão de build.
- **Atualização incremental (delta)** — o app compara os arquivos locais com o manifest pelo
  hash e baixa só o que falta ou mudou.
- **Integridade e reparo** — hash divergente dispara o re-download só daquele asset, então dá
  pra reparar sem baixar tudo de novo.

Os assets ficam anexados como arquivos de release; o manifest é versionado aqui.

> Projeto pessoal / de estudo. Assets distribuídos apenas para usuários autorizados.
