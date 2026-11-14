# Projetos open-source e modelo de custo

Pesquisa de 14/11/2026. Estrelas e atividade vêm da API do GitHub.

## Projetos parecidos

| Projeto | ★ | Licença | IA / conversa | PT-BR |
|---|---|---|---|---|
| [Reactive Resume](https://github.com/reactive-resume/reactive-resume) | 45,7k | MIT | Usa chave própria (vários provedores), mas edita um currículo existente, não cria por conversa | Sim |
| [Resume Matcher](https://github.com/srbhr/Resume-Matcher) | 29,3k | Apache-2.0 | Compara currículo com vaga | Não |
| [RenderCV](https://github.com/rendercv/rendercv) | 18,0k | MIT | Sem IA; gera PDF a partir de YAML (Typst) | Sim |
| [OpenResume](https://github.com/xitanggg/open-resume) | 9,0k | AGPL-3.0 | Sem IA; parado desde 2024 | Não |
| [JSON Resume](https://github.com/jsonresume/jsonresume.org) | — | MIT | Schema e temas | — |
| [meu-emprego-novo](https://github.com/R238Company/meu-emprego-novo) | 257 | MIT | Agentes a partir de vaga e histórico; não é entrevista | Sim |

- **Currículo por conversa:** só há protótipos com 0 a 2 estrelas. Não existe projeto maduro em PT-BR nem focado em primeiro emprego.
- **Dá para reaproveitar:** usar o schema JSON Resume como saída da IA, aproveitar renderizadores ou temas existentes para o PDF e oferecer "abrir no Reactive Resume" para quem quiser editar depois.

## "O usuário paga a IA"

| Caminho | Situação | Atrito para o leigo |
|---|---|---|
| Login com assinatura Claude (Pro/Max) ou Claude Code | **Proibido.** "Anthropic does not permit third-party developers to offer Claude.ai login into their own applications" ([termos](https://code.claude.com/docs/en/legal-and-compliance)) | — |
| [Sign in with ChatGPT](https://developers.openai.com/siwc/token-sharing-open-source) | Permitido para apps open-source **rodando localmente**. App web hospedado depende de [aprovação da OpenAI](https://openai.com/form/sign-in-with-chatgpt-interest/) | Exige ChatGPT Plus |
| [Sign in with Poe](https://creator.poe.com/docs/external-applications/sign-in-with-poe) | Permitido (OAuth) | Usuário grátis não acessa modelos pagos pela API, então exige assinatura |
| [OpenRouter OAuth PKCE](https://openrouter.ai/docs/guides/overview/auth/oauth) | Permitido; a chave e os créditos são do usuário | Criar conta; sem créditos, modelos `:free` com 50 req/dia ([limites](https://openrouter.ai/docs/api/reference/limits)); comprar créditos exige cartão em dólar |
| [Puter.js "user pays"](https://docs.puter.com/user-pays-model/) | Permitido; o desenvolvedor paga US$ 0 | O tamanho da franquia grátis não é publicado; mais um intermediário com acesso a dados pessoais |
| Local (Ollama, WebLLM) | Possível | Inviável para quem só tem celular; modelos pequenos são fracos em PT-BR |

## Custo por currículo (projeto pagando a API)

Estimativa de cerca de 100k tokens de entrada e 6k de saída por currículo (20 trocas, sem cache).

| Modelo (preço oficial por 1M tokens) | Custo por currículo |
|---|---|
| [Claude Haiku 5.5](https://platform.claude.com/docs/en/about-claude/pricing): US$ 0,10 / 0,50 | ≈ US$ 0,013 |
| [Gemini 2.5 Flash-Lite](https://aistudio.google.com/docs/pricing): US$ 0,10 / 0,40 | ≈ US$ 0,012 |
| [gpt-5.6-luna](https://developers.openai.com/api/docs/pricing): US$ 0,20 / 1,20 | ≈ US$ 0,027 |

- **O free tier do Gemini não serve:** os [termos](https://aistudio.google.com/docs/terms) proíbem enviar dados pessoais aos serviços não pagos. A API do Gemini também proíbe serviços "likely to be accessed by" menores de 18, o que é um problema para Jovem Aprendiz (14 anos ou mais).
- **A Anthropic permite atender menores com salvaguardas** ([diretrizes](https://support.claude.com/en/articles/9307344-responsible-use-of-anthropic-s-models-guidelines-for-organizations-serving-minors)).

## Conclusão

- "O usuário traz a própria IA" **não funciona para o público-alvo**: ele não tem chave, créditos nem assinatura.
- O caminho de menor atrito e permitido pelos termos é **o projeto pagar a API de um modelo barato**, cerca de 1 a 3 centavos de dólar por currículo, sem login, com limite por dispositivo e captcha. Chave própria, OpenRouter e versão local ficam como opções para quem é dev e para ONGs.
- O risco real não é o custo de tokens. É abuso, LGPD (inclusive dados de menores) e a dependência de intermediários.
