# Como editar o funil

- Edite o código em `src/site.src.js` (formatado e legível).
- Gere o arquivo publicado: `npm install` (uma vez) e depois `npm run build`. Isso cria o `site.js` minificado que o site carrega.
- Teste local: `npm run serve` e abra http://localhost:8000
- Imagens e áudio ficam em `/images`, `/button-click.mp3`, `/favicon.ico` (hospedados no próprio domínio).

## Fluxo do quiz (versão curta)
inicio → pergunta-1 → pergunta-6 → pergunta-9 → medidas → pergunta-11 → pergunta-12 → diagnostico → cupon → vsl → plano

A ordem fica na constante `Qq` (perguntas usadas) em `src/site.src.js`.

## Eventos do pixel
- `QuizStep` (custom) em cada tela, com `step` e `step_number`
- `QuizComplete` (custom) + `Lead` ao terminar o quiz (tela diagnóstico)
- `AddToCart` ao abrir a VSL; `VslPlay` / `VslPitchReached` no vídeo
- `ViewContent` ao abrir a oferta; `InitiateCheckout` no clique em comprar
