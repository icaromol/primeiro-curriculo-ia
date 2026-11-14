# Go/no-go

**Decisão (14/11/2026): GO.** Antes do planejamento, duas validações (ver abaixo).

Base: `01-tamanho-do-problema.md`, `02-foruns-e-dores.md`, `03-concorrentes.md` e `04-open-source-e-custo.md`.

## Por que seguir

- **Público grande:** cerca de 3,3 mi de jovens de 14 a 24 anos desocupados, de 6 a 8 mi de nem-nem e cerca de 700 mil contratos de Jovem Aprendiz.
- **Demanda comprovada pelo comportamento:** mais de 20 mi de instalações de apps de currículo em PT-BR e buscas crescendo.
- **Os geradores "grátis" que cobram no download são a dor mais bem documentada**, com centenas de reclamações no Reclame Aqui. Ser grátis de verdade e aberto responde a isso.
- **Não existe projeto open-source maduro de currículo por conversa**, nem em PT-BR, nem focado em primeiro emprego.
- **Recrutadores rejeitam currículo "com cara de IA" e exagerado.** Isso abre espaço para um método que transforma experiência informal em currículo honesto, sem inventar nada.

## O que define o projeto

1. **Diferencial:** a metodologia de RH para quem tem zero experiência formal (bico, cuidar de alguém, igreja, escola), com autenticidade acima de texto polido.
2. **PDF livre, sem cadastro e sem amarra a plataforma.**
3. **Open-source hospedável:** ONGs, CRAS, Sine e escolas podem rodar e adaptar.
4. **Custo:** o projeto paga a API de um modelo barato (cerca de 1 a 3 centavos de dólar por currículo), sem login e com limite por dispositivo. Chave própria, OpenRouter e versão local ficam como opção para devs e ONGs.

## Hipóteses descartadas

- **O usuário paga os tokens ou traz a própria IA como caminho principal.** O público-alvo não tem chave, créditos nem assinatura. O login com assinatura Claude é proibido pelos termos da Anthropic. O login com ChatGPT só vale para app local ou com aprovação da OpenAI. O Poe exige assinatura.
- **Free tier do Gemini:** os termos proíbem dados pessoais nos serviços não pagos, e a API proíbe serviços acessados por menores.

## Riscos

- **Vagas.com VcCV:** chat grátis em PT-BR, com áudio, focado em primeiro emprego e baixa alfabetização digital. Ocupa o núcleo da ideia.
- **Anúncios de recrutamento:** a Vagas é concorrente e o público vale pouco para anunciante. Patrocínio e financiamento institucional parecem mais viáveis. Fica em aberto.
- **LGPD:** Jovem Aprendiz começa aos 14 anos, então o produto trata dados de menores (art. 14).
- **"A falta de currículo é a barreira principal" ainda é suposição.** O único dado direto é de 2017 e mostra 23%.

## Validações antes do planejamento

1. **Testar o VcCV.** Se ele exportar PDF livre e lidar bem com experiência informal, o foco passa a ser motor open-source para ONGs e poder público, e não um produto para o consumidor final.
2. **Conversar com 5 a 10 pessoas do público-alvo** (CRAS, ONGs, programas de Jovem Aprendiz).
