---
layout: prose
title: Vellichor — Política de Privacidade
permalink: /pt-BR/legal/privacy/
lang: pt-BR
canonical_en: /legal/privacy/
canonical_es: /es/legal/privacy/
canonical_pt-BR: /pt-BR/legal/privacy/
canonical_de: /de/legal/privacy/
updated: 2026-05-27
---

# Política de Privacidade

**Data de vigência: 2026-05-27**

Esta é a política de privacidade do **Vellichor**, um app de Q&A sobre PDFs para plataformas Apple desenvolvido pela **KhassinX**.

Escrevemos isto em linguagem clara porque queremos que você leia de verdade.

## A versão curta

- **Não coletamos, armazenamos nem transmitimos seus PDFs nem suas consultas sobre eles.** O Vellichor roda os Apple Intelligence Foundation Models no seu aparelho.
- **Não temos analytics, nem SDKs de tracking, nem serviços de terceiros na v1.** Nem Firebase, nem Google Analytics, nem Mixpanel, nem Sentry, nem Crashlytics. Nenhum.
- **Não existe sistema de contas.** Você não precisa se cadastrar, não nos dá um e-mail, não há senha pra esquecer.
- **Sua biblioteca e anotações sincronizam entre seus aparelhos pelo seu próprio iCloud.** A Apple criptografa isso de ponta a ponta; nós nunca vemos.
- **Sua compra é verificada pela Apple, não por nós.** Não guardamos informação de pagamento nem sabemos quanto você pagou.

## Quais dados o Vellichor manipula

### Documentos (seus PDFs)

O Vellichor lê os PDFs que você importa do app Arquivos, do Compartilhar, de scan da câmera, drag-and-drop ou iCloud Drive. Esses documentos são guardados:

- **No seu aparelho**, dentro do container de aplicação do Vellichor
- **No seu iCloud Drive pessoal** sob a pasta do Vellichor, se você ativar o sync via iCloud (pra que os mesmos documentos apareçam nos seus outros aparelhos Apple)

Nós — KhassinX — não temos acesso a esses documentos em nenhum momento. Eles nunca chegam a um servidor que controlemos. Nem chegam aos servidores da Apple num formato que a Apple possa ler; o iCloud Drive usa criptografia ponta a ponta atada ao seu Apple ID.

### Perguntas que você faz e respostas que o Vellichor gera

Quando você faz uma pergunta ao Vellichor sobre um PDF, a pergunta é processada pelos Apple Intelligence Foundation Models rodando localmente no seu iPhone, iPad ou Mac. O modelo produz uma resposta usando o conteúdo do documento como contexto.

- **A pergunta não sai do seu aparelho.**
- **A resposta não sai do seu aparelho.**
- O histórico de conversa fica guardado no seu aparelho (e sincroniza pelo seu iCloud pessoal entre seus aparelhos, se o iCloud estiver ativo).

### Anotações, marcações e notas

Tudo o que você marca — marcações de texto, notas digitadas, escrita à mão com Apple Pencil — é guardado na base privada do CloudKit sob seu Apple ID. A base privada do CloudKit é criptografada ponta a ponta; só seus aparelhos conseguem ler. Nós não.

### Estado de assinatura / compra

O Vellichor usa **StoreKit 2** (o sistema de compras dentro do app da Apple) para o desbloqueo Pro de uma vez. Quando você compra, a Apple confirma a transação diretamente com a App Store do seu aparelho. Não rodamos servidor de pagamento, não guardamos dados de cartão e não sabemos seu nome real, e-mail nem endereço de cobrança. Via a validação anônima de recibo da Apple, conseguimos saber apenas se uma instalação dada comprou o Pro — nada mais.

Family Sharing é suportado: se um membro da sua família comprou o Vellichor Pro, seu aparelho recebe o entitlement automaticamente via Apple.

### Relatórios de crash e diagnósticos

Se o Vellichor travar, o sistema padrão de relatório de falhas da Apple pode incluir um relatório anônimo enviado à Apple **se e somente se você optou por compartilhar via Ajustes do iOS → Privacidade e Segurança → Análise e melhorias → Compartilhar com desenvolvedores de Apps**. É um mecanismo da Apple, não nosso. Recebemos logs de crash agregados, totalmente anônimos, via App Store Connect; não contêm conteúdo de documentos, perguntas, respostas nem informação pessoal identificável.

Se você não optou por compartilhar analytics com a Apple, não recebemos nada.

## Quais dados o Vellichor NÃO manipula

- **Sem SDKs de analytics.** Nem Firebase Analytics, Google Analytics, Mixpanel, Amplitude, Segment, Sentry, Crashlytics, AppsFlyer, Adjust, Branch, Singular, Kochava, Apphud, RevenueCat nem nenhuma outra ferramenta de telemetria de terceiros. Nenhuma.
- **Sem publicidade.** Sem redes de anúncios, sem pixels de tracking, sem coleta de IDFA, sem atribuição SKAdNetwork.
- **Sem logins sociais.** Sem "Entrar com Google", sem SDK do Facebook, sem provedor de identidade de terceiros.
- **Sem IA externa.** O Vellichor só usa Apple Intelligence no aparelho. Na v1 não enviamos seu conteúdo para OpenAI, Anthropic, Google nem nenhum outro provedor de IA.

## Crianças

O Vellichor é classificado 4+ e não contém conteúdo censurável. Não coletamos dados de crianças com conhecimento porque **não coletamos dados de ninguém**.

## Seus direitos

Como não coletamos dados, não há nada que possamos acessar, corrigir, excluir ou exportar a seu pedido. Claro, você pode deletar o app e (separadamente) remover seus dados do iCloud do seu Apple ID a qualquer momento.

Se você vive numa jurisdição com direitos de privacidade específicos (GDPR na UE/Reino Unido, CCPA na Califórnia, LGPD no Brasil, e outros), esses direitos continuam aplicando, mas o efeito prático sobre o Vellichor é mínimo: não somos controladores de dados sobre nada seu.

## Mudanças nesta política

Se algum dia mudarmos esta política, vamos atualizar a "Data de vigência" no topo e publicar a nova versão nesta URL. A versão anterior continua acessível via o histórico de commits do GitHub deste site ([khassinx/vellichor-www](https://github.com/khassinx/vellichor-www)).

Não vamos expandir retroativamente o que coletamos. Se alguma feature futura do Vellichor exigir alguma coleta (por exemplo, um opt-in opcional de bug-reporting), será opt-in e explícita, e esta política será atualizada antes dessa feature sair.

## Contato

- **Dúvidas de privacidade**: [hello@khassinx.com](mailto:hello@khassinx.com)
- **Reportes de segurança**: [security@khassinx.com](mailto:security@khassinx.com) ([política](/pt-BR/security/))
- **Desenvolvedor**: KhassinX
