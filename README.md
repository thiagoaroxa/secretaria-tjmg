# Secretaria — Planejamento Organizacional

Ferramenta de planejamento organizacional para Secretarias Judiciais do **Tribunal de Justiça de Minas Gerais**.

Aplicativo HTML standalone, sem servidor, sem banco de dados externo. Os dados de cada comarca ficam em arquivos JSON na pasta do seu computador que você escolher — um arquivo por comarca.

## Como usar

1. Abra o aplicativo (link da hospedagem no GitHub Pages, ou abra `index.html` localmente em Chrome/Edge/Brave/Opera)
2. Na tela inicial, clique em **"Escolher pasta…"** e selecione uma pasta no seu computador onde os dados serão salvos (sugestão: criar uma pasta dedicada, por exemplo `Documentos/Secretaria`)
3. Clique em **"+ Adicionar nova comarca"** para criar o primeiro cadastro, ou clique numa comarca existente da lista para abrir
4. Trabalhe normalmente — alterações são salvas automaticamente no arquivo JSON correspondente
5. O botão **"Tela inicial"** no header sempre traz você de volta à lista de comarcas

## Funcionalidades

- **Cadastro da equipe** com função (Chefe de Secretaria, Servidor, Comissionado, Terceirizado, Estagiário), área (Cível/Criminal/Ambas), jornada (h/dia × dias úteis/mês) e especialidades
- **Catálogo de tarefas** baseado no Provimento 355/2018-CGJ-TJMG, com volume mensal estimado e esforço médio por execução
- **Atribuições** — titular e reserva por tarefa, com sinalização de tarefas órfãs ou sem reserva (single point of failure)
- **Diagnóstico** — barras de capacidade vs. carga atribuída por integrante, demanda total da Secretaria vs. capacidade da equipe, em horas/mês e em servidores-equivalentes (jornada de referência: 8h × 21d = 168h)
- **Importação de planilhas .xlsx do PJe** — extração automática de atividades, agrupamento por mês, mapeamento das descrições do PJe para as tarefas do catálogo
- **Comparativo de produtividade** entre servidores da Secretaria a partir dos dados importados

## Compatibilidade de navegadores

| Navegador | Modo "pasta vinculada" | Modo "navegador" |
|---|---|---|
| Chrome | ✅ | ✅ |
| Edge | ✅ | ✅ |
| Brave | ✅ | ✅ |
| Opera | ✅ | ✅ |
| Firefox | ❌ | ✅ |
| Safari | ❌ | ✅ |

No modo "navegador" (Firefox/Safari), o aplicativo trabalha com uma comarca por vez salva localmente no navegador. Use Exportar/Importar para mover dados.

## Privacidade dos dados

Os dados ficam **integralmente** no seu computador, na pasta que você escolheu. Nada trafega pela internet, nada é enviado para nenhum servidor. O aplicativo (HTML estático) é hospedado no GitHub Pages, mas os dados nunca saem da sua máquina.

---

*Inspirado e baseado no Manual de Administração Judicial (Haddad & Capanema Pedrosa) e no Provimento 355/2018-CGJ-TJMG.*
