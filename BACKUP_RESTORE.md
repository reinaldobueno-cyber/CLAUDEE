# Backup e Restore rápido

Este repositório foi preparado para publicar a versão atual com rollback simples.

## Backup criado
- `backups/index.backup-83cce3e.html`

## Como restaurar para a versão anterior (estável)

### Opção 1 — Restaurar só o `index.html`
```bash
git checkout 3b9de7b -- index.html
git commit -m "Restore index.html from previous version (3b9de7b)"
```

### Opção 2 — Voltar o repositório inteiro para o commit anterior
```bash
git reset --hard 3b9de7b
```

## Dica de segurança antes de publicar
Crie uma tag de backup do estado atual:
```bash
git tag backup-before-publish-83cce3e
```

Depois faça push da tag:
```bash
git push origin backup-before-publish-83cce3e
```
