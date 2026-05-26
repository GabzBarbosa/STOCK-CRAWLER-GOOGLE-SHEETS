Marketplace Availability Monitor
Problema

Times operacionais de marketplace precisam monitorar manualmente milhares de produtos para identificar:

indisponibilidade,
ruptura de estoque,
páginas removidas,
problemas de catálogo.

Esse processo consome tempo operacional e reduz a capacidade de reação rápida.

Solução

Ferramenta automatizada desenvolvida em Python utilizando Playwright para monitorar URLs de produtos da Netshoes e identificar automaticamente:

produtos disponíveis,
sem estoque,
indisponíveis,
erros HTTP,
sinais de ruptura.

Os resultados são enviados automaticamente para Google Sheets para acompanhamento operacional.

Features
Monitoramento automatizado de URLs
Processamento assíncrono com concorrência controlada
Integração nativa com Google Sheets
Detecção automática de status do produto
Captura de HTTP status
Identificação de páginas indisponíveis
Logs operacionais
Atualização em lote otimizada
Stack
Python
Playwright
AsyncIO
Google Sheets API
Google Colab
Pandas
GSpread
Fluxo Operacional
Google Sheets → Leitura URLs → Navegação automatizada →
Detecção de status → Classificação → Atualização automática
Casos identificados

O sistema identifica automaticamente:

disponível para compra,
sem estoque,
produto indisponível,
erro 404,
páginas removidas,
sinais textuais de ruptura.
Impacto Esperado
redução de trabalho manual,
ganho operacional,
monitoramento em escala,
identificação rápida de indisponibilidade,
apoio à operação de marketplace.
Diferenciais Técnicos
Navegação real via navegador Chromium
Controle de concorrência
Simulação de comportamento humano
Atualização batch no Sheets
Arquitetura assíncrona
Estrutura preparada para escala
Roadmap
Próximas melhorias
Dashboard em tempo real
Alertas automáticos
Integração Slack/Discord
Histórico de variação
Classificação de criticidade
Detecção de mudanças de preço
API de monitoramento
Exportação analítica
Estrutura esperada da planilha
Coluna	Descrição
A	URL
B	Status
C	HTTP Status
D	Título
E	Última verificação
F	Observação
Como executar
Instalação
pip install playwright gspread pandas
playwright install chromium
Execução
await main()
