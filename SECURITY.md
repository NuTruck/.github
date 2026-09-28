# Política de segurança

## Como relatar uma vulnerabilidade

Não abra issue pública para falha de segurança. Escreva para **contato@nutruck.com.br** com o assunto começando em `[SECURITY]`, e descreva:

- o componente afetado (app, API ou painel web) e a versão ou o commit em que você observou o problema;
- os passos para reproduzir, com requisição, payload ou log quando existir;
- o impacto que você consegue demonstrar.

Confirmamos o recebimento em até 3 dias úteis e mantemos você informado até a correção sair.

## Escopo

Entram no escopo os sistemas mantidos por esta organização: o app do motorista, a API, o painel web e o site.

Ficam fora as plataformas de terceiros com as quais o NuTruck se integra, como provedores de SMS e as lojas de aplicativos. Falha encontrada em um desses sistemas deve ser reportada ao fornecedor responsável, e agradecemos se você nos avisar em paralelo quando ela afetar a integração.

Autenticação por código SMS, token de sessão do app, dado financeiro de viagem e dado pessoal tratado sob a LGPD recebem prioridade máxima na triagem.

## O que pedimos

Enquanto avaliamos o relato, não divulgue publicamente, não acesse dado de usuário além do mínimo necessário para demonstrar a falha e não execute teste que degrade o serviço, como negação de serviço ou disparo em massa de SMS.

## Credenciais expostas

Se você encontrar credencial, token ou chave de API versionada em algum repositório, trate como incidente e use o mesmo canal acima. A rotação vem antes da remoção do histórico, porque um segredo que já foi publicado precisa ser considerado comprometido mesmo depois do commit sumir.
