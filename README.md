# Política de Privacidade do Bolsa Família Guia

Última atualização: 19 de outubro de 2026. Esta política descreve o funcionamento da versão 4.8.0 do aplicativo para iPhone.

O Bolsa Família Guia é desenvolvido por Matheus Estoque, responsável pelo tratamento dos dados descritos aqui, sob a marca Estoque Apps. Para dúvidas, pedidos de acesso ou exclusão de dados, escreva para [contato@estoqueapps.com](mailto:contato@estoqueapps.com).

Somos um guia independente. Não representamos o Governo Federal, a CAIXA ou o Ministério do Desenvolvimento e Assistência Social. O app não realiza cadastro no programa, não aprova benefícios e não movimenta dinheiro.

## 1. Quais dados usamos

Usamos apenas os dados necessários às funções escolhidas e ao funcionamento dos serviços de segurança, anúncios e estatísticas descritos nesta política. Não exigimos que você crie um cadastro com nome, e-mail ou senha para consultar ou conversar com o assistente.

- Consulta: NIS informado, mês e ano escolhidos, além dos registros retornados pelo Portal da Transparência. Esses registros podem conter nome, NIS, CPF parcialmente oculto, valor e competência do benefício.
- Chat: pergunta digitada e mensagens recentes da conversa, incluindo informações pessoais que você eventualmente escrever.
- Segurança: identificador de autenticação anônima, contadores de solicitações, horários, tokens de validação do app e informações técnicas da conexão.
- Estatísticas e anúncios: identificadores de instalação e dispositivo, endereço IP, informações do aparelho e sistema, eventos de navegação, impressões e interações com anúncios, além de dados técnicos de diagnóstico e desempenho tratados pelos serviços utilizados.
- Preferências: escolha de lembrar o NIS, avisos já apresentados e registro local de solicitação de avaliação.

O app não solicita acesso a contatos, fotos, câmera, microfone, localização precisa, dados do Saúde ou informações de pagamento. O endereço IP pode permitir aos fornecedores estimar uma localização aproximada.

## 2. Consulta de benefícios

Quando você solicita uma consulta, enviamos o NIS e o período escolhido, por conexão HTTPS, ao nosso serviço no Firebase, que consulta a API do Portal da Transparência. O resultado volta ao aplicativo para exibição.

Nosso backend não grava o NIS nem o resultado da consulta no banco de dados. A aplicação também não inclui esses dados nos registros de erro que produz. A infraestrutura e o serviço público podem manter registros técnicos de acesso conforme suas próprias regras.

Consulte apenas seus próprios dados ou os de uma pessoa que tenha autorizado você a ajudá-la. Os registros públicos podem estar desatualizados e não confirmam saldo disponível para saque. Correções nos registros de origem devem ser solicitadas aos canais oficiais do programa; não podemos alterar a base governamental.

## 3. Chat com inteligência artificial

Antes do primeiro envio de cada conversa, pedimos sua autorização para encaminhar a pergunta e o histórico recente pelo Firebase à OpenAI, fornecedora da inteligência artificial. Você pode recusar ou fechar o aviso: nada daquela conversa será enviado, e as demais funções continuam disponíveis.

Após a autorização, novas perguntas da mesma conversa são enviadas com até 12 mensagens recentes para manter o contexto. Não envie nome, CPF, NIS, documentos, informações de saúde ou outros dados pessoais. O chat não consulta sua situação individual e pode produzir respostas incorretas.

A conversa fica na memória do app enquanto a tela permanece aberta. Nosso backend não a grava no banco de dados. Ao iniciar uma nova conversa, o histórico local é apagado e uma nova autorização é solicitada. Sair da tela ou iniciar outra conversa encerra essa autorização para novos envios, mas não desfaz o processamento já realizado.

A OpenAI pode conservar conteúdo e metadados para prevenção de abusos, normalmente por até 30 dias, com exceções por obrigações legais e segurança. Sua documentação informa que dados da API não são usados para treinamento por padrão, salvo adesão expressa ao compartilhamento. Consulte os [controles de dados da API da OpenAI](https://developers.openai.com/api/docs/guides/your-data) e a [política de privacidade da OpenAI](https://openai.com/policies/privacy-policy/).

## 4. Dados que ficam no aparelho

A opção “Lembrar NIS” é facultativa. Quando ativada, guarda o NIS no armazenamento protegido do iOS, o Keychain. Desativá-la apaga o NIS salvo por essa opção. Dados do Keychain podem persistir após a desinstalação; apague o NIS pela opção do app antes de removê-lo.

Preferências e indicadores de uso ficam no armazenamento local. Instalações atualizadas de versões antigas também podem conservar dados de perfil anteriormente fornecidos, como nome, telefone ou NIS. O app atual não exige preencher esse perfil nem envia esses campos ao backend como cadastro.

Os dados digitados na calculadora, como renda e composição familiar, são processados no aparelho. A seleção de mês e final do NIS no calendário também é local. Não enviamos esses valores ao chat, ao Firebase ou aos anúncios como parte dessas funções.

Se você escolher compartilhar um resultado, o conteúdo indicado na ação será encaminhado ao aplicativo ou destinatário escolhido por você, sujeito às regras desse serviço.

## 5. Autenticação e prevenção de abusos

Usamos Firebase Authentication para gerar uma identidade técnica sem solicitar e-mail ou senha. Esse identificador distingue uma instalação ou sessão de uso, mas não significa que todos os dados sejam anônimos ou impossíveis de relacionar a uma pessoa.

Firebase App Check e Apple App Attest verificam a autenticidade do app. O Firebase e a Apple processam os tokens e informações técnicas necessários a essa verificação.

Mantemos contadores por identificador e função para limitar solicitações abusivas. Esses contadores não contêm NIS, resultados ou mensagens. O prazo de expiração é renovado para dois dias após a última solicitação registrada; a exclusão automática pode ocorrer depois desse prazo devido ao tempo de processamento do serviço. A identidade de autenticação tem ciclo de retenção separado e não é apagada junto com o contador.

## 6. Anúncios e rastreamento

O app utiliza Google AdMob para anúncios de abertura, intersticiais e premiados. O SDK pode tratar dados de dispositivo, IP, identificadores, visualizações, cliques e diagnóstico para entregar anúncios, medir resultados e prevenir fraude. Não enviamos deliberadamente NIS, resultados de consulta ou mensagens do chat como parâmetros publicitários.

No iPhone, solicitamos a permissão de rastreamento do sistema quando o iOS permite apresentar o aviso. A autorização ATT é resolvida antes de inicializar os anúncios na abertura. Se você negar a permissão, o identificador publicitário IDFA não fica disponível para esse rastreamento; os anúncios ainda podem ser exibidos e dados técnicos continuam sendo tratados. Recusar ATT não remove os anúncios nem equivale a recusar toda coleta de dados.

Você pode rever a permissão em Ajustes do iPhone → Privacidade e Segurança → Rastreamento. Para entender a coleta realizada pelo fornecedor, consulte a [política do Google](https://policies.google.com/privacy?hl=pt-BR) e a [descrição de dados do AdMob para iOS](https://developers.google.com/admob/ios/privacy/data-disclosure).

## 7. Estatísticas e configuração do app

Usamos Google Analytics para Firebase para compreender o uso das telas e a exibição de anúncios. Esses eventos podem estar associados a identificadores técnicos; não os descrevemos como dados totalmente anônimos. Não adicionamos NIS, conteúdo do chat ou valores da calculadora aos eventos de análise.

Firebase Remote Config fornece configurações de funcionamento, como ativação e intervalos dos anúncios. Esses serviços podem processar identificadores de instalação, dados de uso e informações do dispositivo. A negativa ao rastreamento ATT não desativa automaticamente essas estatísticas. Saiba mais em [Privacidade e segurança no Firebase](https://firebase.google.com/support/privacy).

## 8. Com quem os dados são compartilhados

O compartilhamento ocorre conforme a função utilizada: Google/Firebase para infraestrutura, autenticação, segurança, configuração e análise; Portal da Transparência para a consulta solicitada; OpenAI para o chat autorizado; Google/AdMob e seus serviços publicitários para anúncios; e Apple para validação do app, permissões do sistema e avaliação na App Store.

Links para canais oficiais, páginas de suporte ou outros aplicativos, como Meu FGTS, abrem serviços com políticas próprias. O link de divulgação do Meu FGTS não transmite automaticamente seu NIS ou sua conversa para esse app.

Podemos tratar o conteúdo de mensagens que você nos enviar por e-mail para atender sua solicitação. Também podemos divulgar informações quando houver obrigação legal ou necessidade legítima de exercer direitos, respeitados os limites da legislação.

## 9. Finalidades e bases legais

Nos termos da [Lei Geral de Proteção de Dados Pessoais](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm), tratamos os dados necessários para prestar o serviço que você solicita. Utilizamos consentimento para o compartilhamento do chat e para permissões que o exigem; legítimo interesse, quando aplicável e respeitados seus direitos, para segurança, prevenção de abusos e melhoria do serviço; e cumprimento de obrigação legal quando necessário.

Não usamos sua aceitação desta política como autorização genérica para qualquer tratamento. Quando uma autorização específica é necessária, ela é solicitada no contexto da função. As estimativas e respostas do app não tomam decisões oficiais sobre concessão, suspensão ou pagamento de benefícios.

## 10. Retenção e transferências internacionais

O NIS lembrado permanece localmente até você apagar a opção; o histórico de chat permanece na tela durante a conversa; e os contadores seguem o prazo descrito na seção 5. Dados técnicos de autenticação, análise, publicidade, segurança e atendimento seguem os prazos e critérios necessários a cada finalidade, às configurações dos serviços e às obrigações aplicáveis. Desinstalar o app não apaga automaticamente registros já tratados pelos fornecedores.

As funções do nosso backend estão hospedadas na região de São Paulo, mas isso não mantém todo o tratamento no Brasil. Serviços do Google, OpenAI, Apple e GitHub podem processar dados em outros países, inclusive nos Estados Unidos. As transferências estão sujeitas às salvaguardas contratuais e aos mecanismos exigidos pela legislação aplicável.

## 11. Segurança e seus direitos

Usamos conexões HTTPS, armazenamento protegido para o NIS salvo, validação do aplicativo e restrição de acesso ao banco de dados. Credenciais dos serviços ficam no servidor. Nenhum sistema é totalmente imune a incidentes; por isso, evite inserir dados pessoais no chat e mantenha o aparelho protegido.

Você pode solicitar confirmação de tratamento, acesso, correção, informação sobre compartilhamento, revogação de consentimento e, quando aplicável, portabilidade, anonimização, bloqueio ou exclusão de dados. Também pode apresentar oposição nas hipóteses legais e procurar a Autoridade Nacional de Proteção de Dados.

Envie o pedido para [contato@estoqueapps.com](mailto:contato@estoqueapps.com), identificando o aplicativo e o que deseja solicitar. Não envie senhas, códigos de verificação ou documentos completos no primeiro contato. Se necessário, solicitaremos somente as informações mínimas para verificar sua legitimidade e localizar os registros. Dados exclusivamente locais podem não estar acessíveis à nossa equipe. Pedidos serão atendidos nos termos e prazos legais, ressalvadas hipóteses de conservação obrigatória.

## 12. Crianças e adolescentes

O app é destinado a pessoas que buscam orientação sobre benefícios e aos responsáveis por famílias. Informações sobre quantidade e faixa etária de dependentes na calculadora são processadas localmente. Não pedimos que crianças enviem documentos ou dados pessoais. Se um responsável identificar tratamento indevido de dados de criança ou adolescente, deve entrar em contato para que o caso seja analisado e sejam tomadas as medidas cabíveis, observando o melhor interesse do titular.

## 13. Esta página e alterações da política

Esta política é hospedada no GitHub Pages. Não adicionamos anúncios, formulários, cookies de análise ou scripts de rastreamento próprios à página. O GitHub pode tratar IP e registros técnicos de acesso para hospedar e proteger o serviço, conforme sua [política de privacidade](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

Atualizações serão publicadas neste endereço com nova data. Mudanças relevantes nas finalidades ou no compartilhamento serão informadas no app quando aplicável, com nova autorização quando necessária. Esta política é específica do Bolsa Família Guia e substitui, para as práticas aqui descritas, a política genérica de aplicativos da Estoque Apps.
