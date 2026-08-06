# openspec-workflow-template

Repo canônico de **overrides** para a skill `maxdev-workflow-sync` (distribuída
via [maxsyncai-opencode-skills](https://github.com/maxsyncai/maxsyncai-opencode-skills)).

## O que vive aqui

Os 7 arquivos canônicos do workflow MaxDev:

```
AGENTS.md · dev-workflow.md · scripts/{close-change.sh, push-safe.sh} ·
openspec/{config.yaml, templates/{design.md, explore-brief.md}}
```

Opcional: `workflow.version` (override da versão da skill v1.0.2+).

## Como atualizar este template

A skill carrega defaults embutidos em `assets/`. Para sincronizar este template
a partir dos `assets/` da skill (sem rodar `sync-workflow.sh` dentro deste repo):

```bash
SKILL=<path>/skills/maxdev-workflow-sync/assets  # path no package instalado
cp $SKILL/AGENTS.md $SKILL/dev-workflow.md .
cp $SKILL/scripts/*.sh scripts/
cp $SKILL/openspec/config.yaml openspec/
cp $SKILL/openspec/templates/*.md openspec/templates/
cp $SKILL/workflow.version workflow.version
git add -A && git commit -m "chore: sync from maxdev-workflow-sync vX.Y.Z"
```

## Documentação completa da skill

Veja `skills/maxdev-workflow-sync/README.md` no repo
[maxsyncai-opencode-skills](https://github.com/maxsyncai/maxsyncai-opencode-skills).