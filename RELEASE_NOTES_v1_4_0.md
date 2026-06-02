IdenVault v1.4.0 — Release Notes
=================================

Release date: 2026-06-02

Resumo
------
- Adicionada integração FUSE para montar cofres como sistemas de arquivos.
- API inicial HTTP local para automação e integrações (endpoints básicos: status, mount/unmount, list).
- Novos comandos CLI: `mount`, `unmount`, `api-start`, `api-stop`, `api-status`.
- Atualizações e melhorias na organização do código, ajustes de build e `.gitignore`.

Detalhes
-------
- FUSE: permite expor um cofre montado no sistema de arquivos para leitura/escrita controlada pelo core.
  - Requisitos: libfuse (Linux) / winfsp (Windows) ou similar; privilégios poderão ser necessários.

- API inicial: servidor HTTP local para executar operações básicas sem usar TUI/CLI diretamente.
  - Endpoints planejados: `/status`, `/v1/vaults`, `/v1/mount`, `/v1/unmount`.

- CLI: novos comandos para controlar FUSE e a API; `help` atualizado com instruções rápidas.

Compatibilidade
-------------
- Esta é uma versão compatível com a série 1.x. Se você depender de implementações internas, teste antes de atualizar.

Upgrade
-------
1. Instale dependências de FUSE apropriadas ao seu sistema.
2. Atualize sua cópia do repositório e execute seus testes locais.

Notas
-----
- Mais documentação será adicionada em `docs/` com exemplos de montagem, permissões e uso da API.

Contato
-------
Report bugs e solicitações de features via Issues no repositório.
