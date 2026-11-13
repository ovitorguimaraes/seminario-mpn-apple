# Roteiro D1 — 10 minutos

Abertura/equipe: 00:00–00:30

Eduardo Eugênio Pereira | 1. Empresa | 00:30–02:00

**Slide 3 · Por trás do universo Apple**

“Esses aparelhos são a parte que a gente vê. Nosso seminário olha para o trabalho por trás do software. Como uma atualização do iOS é preparada? Quem pode acessar os sistemas de desenvolvimento? Essas duas perguntas definem o nosso recorte.”

**Slide 4 · O recorte do seminário**

Apresente o recorte em Sistemas de Informação e os dois processos que o seminário modela. Um deles transforma demandas e falhas em atualizações do iOS. O outro controla quem pode acessar os sistemas de desenvolvimento. O primeiro contribui para a qualidade do produto; o segundo protege o código e mantém as permissões justificadas. Explique que não estamos descrevendo o modelo de receita da empresa nem a jornada de compra do consumidor. Estamos modelando processos organizacionais de apoio à entrega de valor. Os fluxos são propostas acadêmicas aplicadas ao contexto da Apple, permitidas pela orientação do professor. Encerre apresentando a pergunta que orienta o trabalho: quais atividades, decisões, pessoas e sistemas precisam se coordenar para entregar software com qualidade e acesso controlado? Passe a palavra para a pesquisa.

João Vitor de Paula | 2. Pesquisa | 02:00–03:30
Explique o método: pesquisa documental em fontes públicas. O Apple Beta Software Program e o Feedback Assistant mostram que usuários e desenvolvedores podem testar versões e relatar falhas. A documentação de segurança da Apple também descreve mecanismos de autorização e assinatura de atualizações. Essas evidências sustentam o tema do primeiro processo, mas não revelam o fluxo interno completo. Priorização, revisão, testes em paralelo e decisões de liberação são propostas do grupo. Para o segundo processo, usamos como referência conceitual o NIST, especialmente gestão de contas e privilégio mínimo. Isso não comprova que a Apple use exatamente o fluxo apresentado. A periodicidade de 90 dias também é uma escolha acadêmica. A notação segue a BPMN da OMG. Não realizamos entrevistas, não observamos a operação e não coletamos indicadores reais. Portanto, distinguimos evidência pública, referência técnica e proposta de modelagem. Essa separação permite discutir o desenho sem atribuir à empresa procedimentos que não verificamos.

Matheus Felipe Costa | 3. Dois processos | 03:30–05:00
Apresente o limite de cada processo antes de falar das atividades. No P1, a entrada é uma demanda ou falha registrada. A equipe classifica impacto e reproduz o problema quando aplicável, define prioridades e critérios de aceite, implementa e revisa a alteração. A saída pode ser uma release monitorada e encerrada ou um incidente contido que exige uma nova versão. O objetivo é melhorar a confiabilidade e a continuidade do produto. No P2, a entrada é um pedido de acesso a um sistema de desenvolvimento. O ciclo abrange informações do solicitante, avaliação do gestor, políticas de segurança, concessão e acompanhamento. Há encerramento por recusa ou por revogação futura. O objetivo é proteger sistemas e preservar evidências de quem recebeu acesso, por quê e por quanto tempo. Os processos se relacionam: a equipe que desenvolve o iOS precisa de permissões adequadas. Apesar disso, cada modelo tem seu próprio início e seus próprios resultados, evitando um único fluxo excessivamente amplo.

Vitor Guimarães | 4. Critérios, pessoas e sistemas | 05:00–06:30
Use aproximadamente 45 segundos em cada slide de critérios. No iOS, a demanda precisa ter impacto e aceite definidos. Desenvolvimento implementa e revisa. Qualidade e segurança realizam verificações; operação autoriza, distribui e monitora. O critério de liberação é a aprovação das verificações. Um incidente crítico durante a janela de observação leva à contenção. Os sistemas citados representam funções, como repositório, integração contínua e observabilidade, e não ferramentas internas confirmadas da Apple. Na gestão de acessos, o solicitante informa sistema, perfil e justificativa. O gestor avalia a necessidade; segurança verifica privilégio mínimo e conflitos; administração configura acesso, autenticação multifator, validade e evidências. A revisão ocorre em 90 dias por decisão do grupo. Mudança de função ou saída provoca a revogação do perfil anterior. Indicadores possíveis são tempo até a release, incidentes por versão e prazos de concessão e revogação. São propostas de medição, sem resultados coletados.

Guilherme Marques | 5. Desenho do BPMN | 06:30–08:00
Reserve aproximadamente 45 segundos para cada desenho. Primeiro apresente a estrutura: cada piscina contém um processo interno e cada raia indica uma responsabilidade. As setas contínuas mostram a sequência e podem atravessar raias da mesma piscina. Círculo de borda simples marca o início; borda grossa marca o fim; retângulo arredondado representa uma atividade. No desenho do iOS, mostre a passagem de produto para desenvolvimento, depois para qualidade e segurança, e finalmente para operação. Destaque os dois losangos com mais: eles abrem e sincronizam as verificações paralelas. Mostre também o retorno ao desenvolvimento e os dois resultados do monitoramento. No desenho de acessos, identifique solicitante, gestor, segurança e administração. Aponte o retorno para complementar o pedido e as duas decisões de aprovação. No acompanhamento, diferencie o temporizador de revisão do sinal de mudança funcional. Não leia cada caixa. A ideia é apresentar como o desenho organiza o processo; a explicação dos caminhos fica para Jefferson.

Jefferson Marlon Maciel Silva | 6. Explicar o BPMN | 08:00–09:30
No primeiro modelo, explique por que paralelismo não é escolha. Os dois ramos de verificação são executados e o ponto de encontro aguarda ambos. Depois, a decisão exclusiva avalia os resultados: se qualquer critério falhar, a versão retorna ao desenvolvimento, passa pela revisão e repete as verificações. Use o exemplo de uma correção que funciona, mas não atende à segurança. Após a distribuição, um incidente crítico gera contenção e uma nova demanda; não estamos propondo reverter automaticamente o iOS já instalado. No segundo modelo, aprovação do gestor e conformidade de segurança são verificações distintas. Depois de conceder, a execução espera o primeiro evento: revisão em 90 dias ou mudança de função/saída. A revisão pode manter o acesso e reiniciar a espera. A mudança revoga o perfil anterior; uma nova função exige outro pedido. Use o exemplo de transferência de equipe antes dos 90 dias. Conclua que os modelos tornam decisões, retrabalho e responsabilidades explícitos.

Encerramento: 09:30–10:00 — referências para consulta, agradecimento e QR code do repositório.

## Roteiro D2 — Estratégia e processos de negócio

Previsão de **7 minutos**, com trocas e encerramento incluídos. Limite de **10 minutos**. Os tempos abaixo são cumulativos.

| Tempo | Integrante | Slide e assunto |
| --- | --- | --- |
| 00:00–00:45 | Eduardo Eugênio Pereira | Abertura — os dois processos do D1 em uma frase cada |
| 00:45–01:45 | João Vitor de Paula | Missão — qual valor a Apple entrega |
| 01:45–02:45 | Matheus Felipe Costa | Visão — como evoluir com confiança |
| 02:45–04:00 | Guilherme Marques | Valores — privacidade, acessibilidade e meio ambiente |
| 04:00–06:00 | Vitor Guimarães | Metas — o que medir no P1 e no P2 |
| 06:00–07:00 | Jefferson Marlon Maciel Silva | Síntese, referências e agradecimento |

### Eduardo · Da estratégia ao trabalho do dia a dia

- Aponte para o P1 e o P2. No D1, o grupo modelou a liberação de atualizações do iOS e o controle de acesso aos sistemas de desenvolvimento.
- Faça a pergunta que abre o D2. Como as prioridades da empresa viram decisões nesses dois processos? Passe para o João sem reapresentar os BPMNs.

### João · O valor que a Apple entrega

- Explique a missão proposta pelo grupo. Dispositivos, software e serviços funcionam juntos para entregar uma experiência integrada. Use o MacBook do slide como exemplo de como o hardware e os aplicativos trabalham juntos.
- Aponte para os dois blocos. Testar as atualizações ajuda a preservar essa experiência, e restringir o acesso ao código protege o trabalho de desenvolvimento. A formulação é uma síntese a partir do relatório anual.

### Matheus · Um ecossistema que evolui com confiança

- Aponte para “evolui com confiança” e explique a direção proposta pelo grupo. A experiência precisa continuar confiável à medida que versões e equipes mudam.
- No P1, acompanhe a versão depois que ela chega ao usuário para identificar problemas. No P2, use o exemplo de alguém que troca de equipe e precisa ter as permissões antigas revistas.

### Guilherme · Valores na prática

- **Privacidade.** Quem precisa consultar um repositório pode receber leitura, sem permissão para alterar o código.
- **Acessibilidade.** Se uma atualização muda uma tela, confira se o usuário consegue navegar nela com o VoiceOver.
- **Meio ambiente.** Avalie se a correção funciona em aparelhos mais antigos que ainda recebem suporte. Isso ajuda a mantê-los úteis por mais tempo.
- Os três valores são publicados pela Apple. Os exemplos mostram como o grupo os aplicou aos processos modelados.

### Vitor · Da intenção à medição

- **04:00–04:20 · Gancho.** “A gente viu quais valores orientam as decisões. Agora, como saber se essas decisões estão sendo cumpridas?” Aponte para a linha do piloto de **90 dias**.
- **04:20–05:00 · P1, 100%.** Aponte para o primeiro número. Em cada liberação, a Operação verifica se há registro de aprovação funcional e de segurança. Exemplo de ensaio: se houve 10 liberações e 9 tinham os dois registros, o resultado foi **90%** e ficou abaixo da meta.
- **05:00–05:45 · P2, 95% em 24 horas.** Aponte para o segundo número. O prazo começa quando a saída ou a mudança de função é registrada. A Administração de acessos divide as permissões revogadas no prazo por todas as que precisavam ser revogadas. Se 19 de 20 foram retiradas no prazo, deu **95%**. A permissão pendente continua na conta.
- **05:45–06:00 · Passe a palavra.** Diga que os números são metas do piloto acadêmico. “Essas duas medidas mostram onde verificar se o processo está cumprindo o que foi combinado.”

### Jefferson · Síntese, referências e obrigado

- Até **06:40**, faça a síntese em uma ideia: missão e visão dão direção, valores orientam decisões e metas permitem verificar se essas decisões foram cumpridas.
- Passe pelas referências em uma frase. O relatório e os valores da Apple fundamentam a estratégia, e as referências técnicas apoiam os exemplos. Avance para **Obrigado** e encerre até **07:00**.
