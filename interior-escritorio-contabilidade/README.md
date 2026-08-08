# Design de Interiores — Escritório de Contabilidade

Projeto para gerar conceitos visuais (renders/moodboards) dos ambientes do
escritório de contabilidade, usando o skill [`banana-claude`](../banana-claude)
já vendorizado neste repositório.

Estilo definido: **Corporativo Moderno** — linhas limpas, tons neutros, vidro
e madeira clara. Transmite profissionalismo e confiança.

## Como usar

Este projeto **não gera imagens sozinho** — ele prepara tudo para que a
geração seja rápida usando o Claude Code local com o plugin `banana-claude`
instalado e uma API key do Gemini configurada.

1. No seu terminal (fora deste ambiente remoto), clone o repositório e entre
   na pasta do plugin:
   ```bash
   git clone https://github.com/Caires7/agropec.git
   cd agropec/banana-claude
   claude --plugin-dir .
   ```
2. Configure a API key (uma vez):
   ```
   /banana setup
   ```
3. Carregue o preset de marca do escritório (ver `preset.json` — copie o
   conteúdo para `~/.banana/presets/escritorio-contabilidade.json`):
   ```bash
   mkdir -p ~/.banana/presets
   cp ../interior-escritorio-contabilidade/preset.json ~/.banana/presets/escritorio-contabilidade.json
   ```
4. Gere cada ambiente usando os prompts prontos em `prompts/` — copie e cole
   o texto do prompt (seção "Prompt para o banana-claude") no comando:
   ```
   /banana generate "<cole o prompt aqui>"
   ```
   Ou peça variações:
   ```
   /banana batch "<prompt>" 3
   ```
5. Salve as imagens geradas na pasta `output/<nome-do-ambiente>/` para manter
   tudo organizado (a pasta já existe, vazia, pronta para receber os
   arquivos).

## Estrutura

| Arquivo/pasta | Conteúdo |
|---|---|
| `briefing.md` | Direção de estilo, paleta de cores, materiais, referências |
| `preset.json` | Preset de marca do banana-claude (cores, estilo, iluminação) |
| `prompts/` | Um prompt pronto por ambiente do escritório |
| `output/` | Onde salvar as imagens geradas (não versionadas — ver `.gitignore`) |

## Ambientes cobertos

1. Recepção
2. Sala de atendimento ao cliente
3. Sala de reuniões
4. Estações de trabalho (equipe de contadores)
5. Sala do sócio/contador responsável
6. Copa / área de descompressão

## Referência de estilo

Âncoras editoriais usadas nos prompts (aumentam a qualidade do resultado):
"Architectural Digest interior", "Dezeen office feature", "Wallpaper* design
editorial".
