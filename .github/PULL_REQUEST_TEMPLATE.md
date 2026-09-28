## O que muda

<!-- Qual problema isso resolve? Descreva o comportamento antes e depois, não só os arquivos tocados. -->

## Por quê

<!-- Contexto, issue relacionada, decisão que motivou a mudança. -->

Closes #

## Como testar

<!-- Passos para o revisor reproduzir. Inclua rota, tela do app, usuário de teste ou payload quando fizer sentido. -->

1.
2.

## Checklist

- [ ] A base deste PR é `develop` (nunca `main`)
- [ ] Testes verdes (`php artisan test --compact` ou `npm test`)
- [ ] Lint e formatação sem pendências
- [ ] Documentação atualizada junto da mudança
- [ ] Mudança de contrato da API é compatível com a versão do app que está nas lojas
- [ ] Nenhuma credencial, token ou IP de servidor no diff

## Impacto em produção

<!-- Precisa de migration, variável de ambiente nova, build novo do app ou reprocessamento de fila? Se não, escreva "nenhum". -->
