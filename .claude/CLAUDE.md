# Diretrizes Globais do Projeto

## Trava do Modelo
- **Model Standard:** `claude-sonnet-5`
- **Temperature:** `0.2` (para reduzir variabilidade em OCR e sumarização)

## Regras de Otimização Operacional
1. **Silêncio de Execução:** Não gere explicações nem textos de cortesia entre as etapas do pipeline. Retorne apenas o status de conclusão de cada arquivo/etapa.
2. **Processamento em Batch por Diretório:** Processe um diretório por vez para evitar estouro de contexto visual.
3. **Padrão Obrigatório de Nomenclatura:**
   - Transcrição unificada: `aula-{materia}-{diaaula}-transcricao.txt`
   - Resumo: `aula-{materia}-{diaaula}-resumo.txt`
   - Sumário: `aula-{materia}-{diaaula}-sumario.txt`
4. **Sub-Agentes:** Invoque exclusivamente os agentes declarados na pasta `.claude/agents/` sem alterar os prompts do sistema.