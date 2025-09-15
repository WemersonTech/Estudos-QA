\# Bug Report - Botão "Enviar" do formulário de contato não envia requisição



\*\*Resumo\*\*

Ao preencher o formulário de contato e clicar em "Enviar", a página não faz nenhuma requisição e não exibe mensagem de sucesso ou erro.



\*\*Ambiente\*\*

\- Ambiente: staging

\- Versão / build: 2025.09.15

\- URL: https://site-exemplo.com/contact

\- Browser: Chrome 116.0.5845.96 (Windows 10)

\- Rede: Wi-Fi doméstica



\*\*Passos para reproduzir\*\*

1\. Acessar `https://site-exemplo.com/contact`  

2\. Preencher "Nome" com `Wemerson Silva`  

3\. Preencher "E-mail" com `wemerson@example.com`  

4\. Preencher "Mensagem" com `Teste de formulário - bug`  

5\. Clicar no botão \*\*Enviar\*\*



\*\*Resultado esperado\*\*

\- O formulário envia uma requisição POST para `/api/contact`, exibe uma mensagem de sucesso e limpa os campos do formulário.



\*\*Resultado atual\*\*

\- Ao clicar em \*\*Enviar\*\*, o botão mostra efeito visual, mas nenhuma requisição é observada na aba Network do DevTools. A página não exibe mensagem de erro nem de sucesso; os campos permanecem preenchidos.



\*\*Evidências\*\*

\- Screenshot (ex.: `assets/img/screenshot-bug-contact.png`) — captura da página após clicar em Enviar.  

\- Console (trecho):

- Observação: Network tab não mostra chamada POST para `/api/contact`.



\*\*Severidade:\*\* Média  

\*\*Prioridade sugerida:\*\* Alta



\*\*Passos de triagem sugeridos\*\*

\- Reproduzir o bug em outro browser (Firefox) e em outro ambiente (dev) para confirmar que não é ambiente específico.  

\- Se reproduzido, atribuir para o desenvolvedor responsável pelo componente de formulário.



\*\*Possível causa / sugestão de correção\*\*

\- Possível erro em validação JS (`trim` chamado em variável indefinida) bloqueando a execução do handler que dispara a requisição. Verificar `form-handler.js` linha ~45 e checar guard clauses antes de chamar `.trim()`. Conferir também handlers de submissão (preventDefault) e se o evento do botão está ligado corretamente.



\*\*Reporter:\*\* WemersonTech  

\*\*Data:\*\* 2025-09-15





