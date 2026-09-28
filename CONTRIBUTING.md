# Como contribuir

Estas regras valem para todos os repositórios da organização NuTruck. Quando um repositório tiver regra própria, ela está no `CLAUDE.md` da raiz dele e prevalece sobre este documento.

## Fluxo de branches

`main` é produção estável e `develop` é a linha de trabalho. A regra que não se quebra: **pull request sempre com base em `develop`, nunca em `main`**.

Nomeie a branch pelo tipo do trabalho: `feat/`, `fix/`, `chore/`, `docs/`. Toda feature começa com uma especificação revisada antes da implementação.

O merge do pull request é sempre ação humana. Ninguém faz push direto em `main`, e isso inclui assistentes de IA.

## Antes de abrir o pull request

Os hooks do husky já rodam no commit, mas confira antes de pedir revisão.

**API e painel (`nutruckv2`)** — os testes rodam em PostgreSQL, nunca em SQLite:

```bash
docker compose up -d --wait
php artisan test --compact
vendor/bin/pint --dirty
```

**App (`nutruck-mobile`)**:

```bash
npm run lint
npm run typecheck
npm test
```

## O que todo pull request precisa ter

- Descrição do problema resolvido, não só do que mudou no código.
- Documentação atualizada junto da mudança, quando ela altera comportamento ou contrato da API.
- Teste cobrindo o caminho novo.

## Dinheiro e viagens fechadas

Valor monetário passa sempre pelo cast, nunca por divisão ou multiplicação por 100 no meio do código. Viagem fechada e pagamento realizado não aceitam alteração retroativa: correção entra como lançamento oposto (estorno), nunca como edição ou exclusão.

## Commits

Conventional Commits em inglês, só com o cabeçalho: `type(scope): short description`. Tipos aceitos: `feat`, `fix`, `chore`, `docs`, `refactor`, `perf`, `test`, `build`, `ci`, `style`, `revert`. O commitlint barra o que fugir disso.

## Segurança

Nunca commite credencial, token, chave de API ou IP de servidor, nem em arquivo de exemplo. Variável `EXPO_PUBLIC_*` vai para dentro do bundle do app e não pode guardar segredo. Se encontrar algo desse tipo já versionado, siga a [política de segurança](SECURITY.md) em vez de abrir issue pública.
