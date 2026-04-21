# Game Design Document (GDD)
## Guardiões de Pindorama

**Versão do documento:** 1.0  
**Natureza do documento:** apresentação técnico-pedagógica do projeto  
**Base de análise:** estrutura funcional do projeto, organização de assets, lógica de cenas, sistemas implementados e arquitetura observada no protótipo jogável  
**Tecnologia-base:** Python e Pygame

---

## 1. Apresentação do projeto

**Guardiões de Pindorama** é um jogo digital em 2D, desenvolvido com a biblioteca Pygame, concebido para articular linguagem lúdica, progressão narrativa, desafios interativos e mediação de conhecimentos em uma mesma experiência. O projeto se insere no campo dos jogos sérios e das propostas de aprendizagem gamificada, ao integrar objetivos formativos à estrutura de aventura, exploração, combate, diálogo e resolução de desafios.

A análise do protótipo evidencia um jogo centrado na jornada de um jovem protagonista convocado a restaurar o equilíbrio de Pindorama, território simbólico marcado por referências culturais brasileiras, pela presença da ancestralidade e por elementos narrativos ligados à relação entre natureza, coletividade e responsabilidade. Em termos de desenvolvimento, o projeto já demonstra organização modular, definição de fluxo de cenas, persistência de progresso, sistema de diálogos, quizzes integrados à narrativa, combate em tempo real, enfrentamento de chefe e uso de mapa como dispositivo de progressão.

Trata-se, portanto, de um projeto que ultrapassa a dimensão de entretenimento isolado e se apresenta como artefato digital capaz de ser analisado sob duas perspectivas complementares: a perspectiva técnica, voltada à arquitetura, aos sistemas e à implementação jogável; e a perspectiva pedagógica, relacionada à mediação de conteúdos, ao engajamento do estudante e à integração entre narrativa, ação e aprendizagem.

---

## 2. Finalidade deste documento

Este GDD tem como finalidade sistematizar, de forma clara e formal, os principais elementos constitutivos do jogo, organizando informações relevantes para análise institucional, acadêmica e técnica do projeto. O documento busca:

- apresentar o conceito geral do jogo;
- registrar a estrutura de funcionamento observada no protótipo;
- descrever as principais mecânicas, fluxos e sistemas implementados;
- evidenciar a intencionalidade pedagógica presente na experiência;
- oferecer uma visão de conjunto que apoie avaliação, continuidade do desenvolvimento e refinamento futuro.

---

## 3. Conceito central

O projeto se estrutura como uma aventura narrativa em 2D, na qual o jogador assume o papel de um jovem guerreiro encarregado de enfrentar uma ruptura no equilíbrio sagrado de Pindorama. A progressão ocorre por meio da travessia de áreas, da interação com personagens orientadores, do enfrentamento de ameaças e da superação de provas que articulam ação e conhecimento.

O conceito central do jogo está apoiado em quatro eixos principais:

### 3.1 Narrativa de restauração
A trajetória do jogador é organizada em torno de uma missão de reparação. O desaparecimento ou a usurpação de um artefato sagrado desencadeia o conflito central e justifica a jornada do protagonista por diferentes regiões e desafios.

### 3.2 Experiência lúdica com progressão
O jogo propõe avanço gradual por cenas, fases e áreas desbloqueáveis, valorizando a sensação de percurso, conquista e ampliação de mundo.

### 3.3 Integração entre ação e aprendizagem
Os elementos pedagógicos não aparecem como anexos externos à jogabilidade, mas como parte do próprio fluxo da experiência. Questões, diálogos e decisões narrativas são utilizados como mecanismos de continuidade, compreensão e validação do avanço do jogador.

### 3.4 Valorização de referências culturais brasileiras
O universo ficcional mobiliza símbolos, personagens, criaturas e elementos de matriz cultural brasileira, especialmente associados à ancestralidade, aos saberes tradicionais e à relação entre ser humano e natureza.

---

## 4. Gênero, escopo e posicionamento

### 4.1 Gênero principal
- Aventura 2D
- Ação com progressão narrativa
- Jogo sério de caráter educativo

### 4.2 Subgêneros e aproximações funcionais
- plataforma lateral com exploração;
- narrativa guiada por diálogos e eventos;
- quiz contextualizado;
- progressão por mapa;
- combate em tempo real com chefe de fase.

### 4.3 Escopo atual do protótipo
A versão analisada apresenta um recorte funcional consistente, com cenas iniciais, menu, fluxo de seleção, mapa, ao menos duas fases jogáveis, sistema de pausa, persistência de progresso, diálogos encadeados, sistema de decisão e enfrentamento de boss.

### 4.4 Público de interesse
O projeto se mostra especialmente pertinente para:

- estudantes em contexto de aprendizagem mediada por tecnologia;
- professores, pesquisadores e avaliadores interessados em jogos sérios;
- bancas acadêmicas e comissões de análise técnica de projetos educacionais digitais.

---

## 5. Objetivos do projeto

### 5.1 Objetivo geral
Desenvolver um jogo digital autoral que una progressão narrativa, ação, exploração e desafios de conhecimento, promovendo uma experiência significativa tanto do ponto de vista lúdico quanto do ponto de vista formativo.

### 5.2 Objetivos técnicos
- estruturar um jogo modular em Python/Pygame com fluxo de cenas bem definido;
- implementar sistemas de controle, HUD, pausa, save e progressão por mapa;
- organizar ativos visuais e lógicas de fase de modo escalável;
- consolidar um protótipo jogável apto a testes, análise e expansão.

### 5.3 Objetivos pedagógicos
- inserir conteúdos e referências culturais em um ambiente interativo e contextualizado;
- favorecer engajamento por meio de narrativa, desafio e feedback imediato;
- estimular aprendizagem integrada ao percurso do jogador;
- demonstrar a aplicabilidade de jogos digitais como estratégia de mediação de conhecimentos.

---

## 6. Estrutura geral da experiência

O fluxo principal identificado no projeto pode ser compreendido como uma sequência articulada entre preparação, navegação, progressão e validação do avanço do jogador.

### 6.1 Fluxo macro
1. acesso à experiência por tela inicial;
2. navegação pelo menu principal;
3. entrada em sistemas de seleção e preparação;
4. deslocamento ao mapa de progressão;
5. escolha e acesso a uma fase;
6. interação com narrativa local, desafios e combate;
7. conclusão da área e registro do progresso;
8. retorno ao mapa para continuidade da jornada.

### 6.2 Fluxo micro dentro das fases
Durante as fases, o jogador alterna entre deslocamento, leitura de situação, interação, enfrentamento, resolução de questões e observação de feedbacks visuais. Essa alternância confere ritmo à experiência e favorece a combinação entre tensão, leitura e tomada de decisão.

---

## 7. Estrutura de cenas

A arquitetura do projeto evidencia uma organização por cenas, o que favorece clareza no fluxo do jogo e separação funcional entre telas e sistemas.

### 7.1 Login
A cena inicial cumpre papel de entrada no sistema. Ainda que determinados elementos de autenticação estejam simplificados no estado atual do protótipo, essa tela já configura um ponto de acesso institucional e funcional ao jogo.

### 7.2 Menu principal
O menu principal organiza o primeiro contato do usuário com a experiência. Nele se concentram opções essenciais, como iniciar o jogo, acessar configurações e encerrar a execução. A composição visual reforça a identidade do projeto e orienta o jogador para o início da jornada.

### 7.3 Seleção de personagem
A estrutura do projeto aponta para uma etapa de escolha de personagem, vinculada à identidade jogável e à organização do avanço posterior. Esse ponto possui relevância tanto mecânica quanto simbólica, pois demarca o vínculo entre jogador e avatar.

### 7.4 Mapa
O mapa atua como sistema de ordenação da progressão. Sua função é representar visualmente as áreas disponíveis, indicar conclusão de territórios e bloquear regiões finais até o cumprimento dos requisitos previstos.

### 7.5 Fases jogáveis
As fases concentram a maior densidade de jogabilidade. Nelas ocorrem movimentação, interação com personagens, desenvolvimento narrativo, resolução de quizzes, combate e atualização do estado global do jogo.

### 7.6 Pausa e sobreposição de interface
O sistema de pausa interrompe a jogabilidade sem romper a experiência. Além de contribuir para usabilidade, abre espaço para expansão de funcionalidades como inventário, navegação complementar ou opções contextuais.

### 7.7 Game Over
A presença de uma cena específica para falha ou derrota reforça o ciclo de tentativa, erro, aprendizagem e retomada, aspecto importante em jogos com componente de progressão e desafio.

---

## 8. Personagem jogável

O protagonista identificado no projeto, referido como **Jovem Guerreiro**, exerce função central na articulação entre narrativa, ação e progressão.

### 8.1 Papel funcional
- avatar principal do jogador;
- agente de deslocamento e exploração;
- sujeito das interações narrativas;
- participante direto dos desafios pedagógicos;
- combatente nas situações de enfrentamento.

### 8.2 Ações observadas no protótipo
A estrutura de sprites, estados e arquivos de cena indica que o personagem já opera com um conjunto expressivo de ações, incluindo:

- movimentação lateral;
- salto;
- ataque;
- defesa/bloqueio;
- roll ou dash;
- interação;
- progressão de diálogos;
- participação em desafios e combates.

### 8.3 Relevância de design
A construção do personagem jogável demonstra preocupação com legibilidade de ação, clareza de resposta e variedade de estados. Isso contribui para uma experiência mais estável, especialmente em um projeto que precisa conciliar combate, navegação e leitura de elementos pedagógicos.

---

## 9. Mecânicas principais

### 9.1 Exploração
A exploração está vinculada ao deslocamento pelo cenário e à descoberta progressiva dos eventos da fase. Seu papel não é apenas espacial, mas também narrativo, pois é por meio dela que o jogador encontra pontos de ativação, diálogos e desafios.

### 9.2 Combate
O combate aparece como mecânica de tensão e prova de domínio. A combinação entre ataque, defesa, salto e deslocamento lateral configura uma base de ação simples, porém suficiente para sustentar confrontos com significado dramático.

### 9.3 Interação narrativa
Diálogos estruturados por falas, imagens e sequência de eventos exercem papel decisivo na compreensão do mundo do jogo. A narrativa não é tratada como camada secundária, mas como parte do avanço do sistema.

### 9.4 Quiz integrado
O sistema de questões é um dos elementos mais relevantes do ponto de vista pedagógico. Ao ser incorporado ao fluxo de fase, o quiz deixa de assumir formato isolado e passa a operar como prova contextualizada de aprendizagem.

### 9.5 Decisão narrativa
A presença de escolhas em determinados pontos da experiência amplia a agência do jogador, fortalece a sensação de percurso e permite modular a linearidade do avanço.

### 9.6 Progressão por mapa
O uso de mapa com desbloqueio de áreas fortalece a percepção de jornada e organiza de modo claro a estrutura macro do jogo.

---

## 10. Sistema de combate e desafio

O sistema de combate identificado no projeto demonstra uma abordagem funcional voltada à ação em tempo real, com forte apoio em animações de estado e feedbacks visuais.

### 10.1 Estrutura do combate
O jogador utiliza recursos básicos de ataque, defesa e mobilidade para enfrentar ameaças presentes nas fases. Essa estrutura, embora objetiva, é adequada ao estágio do protótipo e oferece base suficiente para polimento posterior.

### 10.2 Enfrentamento de boss
A presença do **Mapinguari** como chefe de fase estabelece um marco importante na progressão do jogo. O boss não atua apenas como obstáculo mecânico, mas como elemento de forte função narrativa, ampliando tensão, exigência técnica e densidade simbólica da experiência.

### 10.3 Valor para a experiência
O combate contribui para:

- variação de ritmo;
- elevação gradual da dificuldade;
- materialização do conflito narrativo;
- reforço do caráter de aventura;
- equilíbrio entre leitura, decisão e ação.

---

## 11. Narrativa e universo do jogo

A narrativa de **Guardiões de Pindorama** apresenta uma organização mítica, com forte presença de símbolos de ruptura, restauração, ancestralidade e missão.

### 11.1 Premissa dramática
O desaparecimento de um elemento sagrado compromete o equilíbrio do mundo e justifica a jornada do protagonista. A experiência é conduzida por personagens orientadores, encontros com ameaças e eventos que articulam prova, aprendizagem e escolha.

### 11.2 Personagens de destaque
#### Cacique
Cumpre papel de orientador, mediador narrativo e agente de convocação. Sua presença organiza a entrada do jogador no conflito central e legitima a missão.

#### Mapinguari
Atua como antagonista ou prova dramática relevante. Sua inserção amplia o conflito e torna mais evidente a combinação entre mito, desafio e progressão.

### 11.3 Temas predominantes
- equilíbrio entre humanidade e natureza;
- responsabilidade coletiva;
- ancestralidade;
- valorização de saberes culturais;
- travessia, prova e amadurecimento.

### 11.4 Estrutura narrativa observada
A organização dos diálogos e eventos indica uma narrativa progressiva, em que introdução, validação do protagonista, confronto e decisão aparecem como etapas articuladas do percurso.

---

## 12. Dimensão pedagógica

A relevância pedagógica do projeto se manifesta não apenas pelo tema abordado, mas pela forma como conteúdos e desafios são inseridos no próprio design da experiência.

### 12.1 Integração entre aprendizagem e jogabilidade
Os conteúdos trabalhados pelo jogo aparecem incorporados à ação, ao diálogo e ao sistema de perguntas. Isso favorece uma aprendizagem contextualizada, na qual o jogador precisa compreender, lembrar, associar e responder para avançar.

### 12.2 Natureza dos desafios
Os quizzes observados tratam de temas culturais e de conhecimentos relacionados à temática da fase. Assim, a progressão depende de um duplo movimento: domínio das mecânicas do jogo e mobilização de saberes.

### 12.3 Potencial formativo
O projeto apresenta potencial para:

- ampliar engajamento do estudante;
- estimular aprendizagem por desafio e feedback;
- valorizar repertórios culturais brasileiros;
- demonstrar possibilidades concretas de aplicação de jogos digitais em contextos pedagógicos.

### 12.4 Relevância para análise institucional
Sob o ponto de vista avaliativo, o jogo evidencia uma tentativa consistente de superar a dicotomia entre “conteúdo” e “entretenimento”, propondo uma experiência em que ambos os aspectos se sustentam mutuamente.

---

## 13. Progressão e estrutura do mundo

A progressão do jogo é organizada por áreas e controlada por sistema de estado global.

### 13.1 Organização por áreas
A estrutura observada indica áreas iniciais e ao menos uma área final condicionada ao cumprimento prévio de requisitos. Esse desenho favorece clareza de meta e ordenação da jornada.

### 13.2 Área final bloqueada
A referência à região **Propugnáculo Além-Mar** como área final demonstra a existência de um objetivo macro de progressão, funcionando como horizonte de conquista do percurso.

### 13.3 Valor de design
Essa estrutura é relevante porque:

- incentiva continuidade;
- organiza ritmo de descoberta;
- permite expansão futura com novos territórios;
- fortalece a sensação de campanha ou jornada.

---

## 14. Interface, HUD e feedback visual

A interface do projeto revela um esforço consistente de mediação visual entre jogador e sistema.

### 14.1 Elementos identificados
- menu principal com navegação por cursor;
- HUD do jogador;
- HUD do boss;
- retratos e imagens de diálogo;
- telas de estado, como pausa e game over;
- feedbacks específicos para respostas corretas e incorretas.

### 14.2 Função comunicacional
A interface exerce papel central na legibilidade da experiência, especialmente por se tratar de um jogo que combina movimentação, combate e leitura de informação pedagógica.

### 14.3 Qualidade observada
A organização dos elementos indica preocupação com molduras, enquadramento, reforço imagético e clareza de estados, o que contribui para uma experiência mais compreensível e visualmente coesa.

---

## 15. Controles e acessibilidade funcional

O projeto foi concebido para operar com teclado e joystick, o que amplia possibilidades de uso e demonstra maturidade técnica no tratamento da entrada do jogador.

### 15.1 Suportes identificados
- teclado;
- controle com mapeamentos específicos;
- compatibilidade com diferentes perfis de joystick.

### 15.2 Importância técnica
A existência de suporte a múltiplos dispositivos fortalece testes, amplia flexibilidade de uso e contribui para a qualidade do protótipo enquanto produto jogável.

### 15.3 Relevância pedagógica indireta
Ao diversificar formas de acesso e controle, o projeto amplia potencial de uso em contextos diferentes, inclusive em ambientes de demonstração, laboratório e apresentação institucional.

---

## 16. Direção de arte e identidade visual

A direção de arte observada no projeto constitui um dos seus pontos de maior personalidade.

### 16.1 Características gerais
O jogo apresenta composição visual autoral em 2D, com uso de sprites, molduras, telas ilustradas, retratos de personagem, camadas de cenário e HUDs específicos.

### 16.2 Identidade estética
A estética reforça atmosfera de aventura mítica e de valorização cultural. A presença de personagens como o Cacique e o Mapinguari, somada ao trabalho de cenários e elementos de interface, contribui para uma linguagem visual própria.

### 16.3 Implicação para o projeto
Do ponto de vista técnico e comunicacional, a arte não atua apenas como adorno, mas como componente estrutural da identidade do jogo, favorecendo reconhecimento, imersão e coerência temática.

---

## 17. Estrutura técnica do desenvolvimento

A arquitetura do projeto demonstra organização modular e preocupação com manutenção.

### 17.1 Base tecnológica
- linguagem: Python;
- biblioteca principal: Pygame;
- organização por scripts, dados e assets.

### 17.2 Elementos estruturais identificados
- arquivo central de inicialização e loop;
- sistema de cenas;
- controle de estado global;
- dados separados para diálogos, decisões e questões;
- assets organizados por função;
- persistência por arquivo JSON.

### 17.3 Mérito técnico do protótipo
A existência de modularização entre lógica, interface, conteúdo e persistência demonstra consistência de desenvolvimento e fornece boa base para evolução futura.

---

## 18. Persistência, estado global e continuidade

O sistema de save e estado global é um recurso essencial no projeto, pois garante continuidade da experiência e coerência da progressão.

### 18.1 Funções observadas
- registro de áreas concluídas;
- armazenamento de flags e condições de jogo;
- persistência de dados em arquivo;
- suporte à retomada da jornada.

### 18.2 Importância para o design
Esse sistema permite ao jogo operar como experiência progressiva, e não apenas como conjunto de cenas isoladas. Isso é fundamental para um projeto cujo sentido depende de percurso, desbloqueio e continuidade narrativa.

---

## 19. Estado atual do desenvolvimento

Com base na versão analisada, o projeto já apresenta um estágio de desenvolvimento significativamente estruturado.

### 19.1 Elementos consolidados
- identidade temática definida;
- fluxo principal de navegação implementado;
- menu e cenas funcionais;
- personagem jogável com estados e ações;
- sistema de diálogo e quiz em funcionamento;
- boss de fase implementado;
- progressão por mapa;
- persistência de progresso;
- suporte a múltiplas formas de controle.

### 19.2 Aspectos ainda passíveis de refinamento
- documentação formal mais ampla;
- polimento de fluxo completo;
- balanceamento de combate;
- padronização final de assets e nomenclaturas;
- consolidação da lore e das descrições institucionais do projeto.

---

## 20. Potencial de expansão

O projeto apresenta base consistente para crescimento em múltiplas frentes.

### 20.1 Expansão de conteúdo
- novas áreas e fases;
- ampliação do mapa;
- novos personagens e variações jogáveis;
- novos bosses e eventos narrativos.

### 20.2 Expansão pedagógica
- ampliação dos conteúdos trabalhados;
- diversificação dos tipos de desafio;
- vinculação com trilhas formativas específicas;
- aprofundamento da mediação de repertórios culturais.

### 20.3 Expansão técnica
- refinamento de interface;
- melhoria do pipeline de assets;
- otimizações de publicação;
- consolidação de documentação para manutenção e continuidade.

---

## 21. Considerações analíticas finais

**Guardiões de Pindorama** apresenta-se como um projeto de desenvolvimento autoral com identidade temática definida, arquitetura funcional consistente e clara intencionalidade pedagógica. A análise do protótipo indica que o jogo já ultrapassou uma etapa meramente conceitual e se encontra em um estágio no qual as principais estruturas de navegação, jogabilidade e progressão estão estabelecidas.

Do ponto de vista técnico, o projeto demonstra capacidade de organização modular, integração entre cenas, persistência de progresso, suporte a diferentes entradas de controle e implementação de sistemas que sustentam uma experiência jogável significativa. Do ponto de vista pedagógico, destaca-se a forma como narrativa, quiz, diálogo e referências culturais são incorporados ao design, evidenciando uma proposta de aprendizagem integrada ao ato de jogar.

Em síntese, trata-se de um projeto com mérito técnico e relevância formativa, cuja continuidade tende a fortalecer ainda mais seu valor acadêmico, institucional e educacional. O desenvolvimento observado revela coerência entre intenção, estrutura e aplicação, configurando um caso promissor de articulação entre tecnologia, design de jogos e mediação pedagógica.
