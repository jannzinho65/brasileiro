Documento Informativo (README)
​Código de Conduta
​Contribuição
​Licença
​Segurança
​Prévia
​⚠️ AVISO DE SEGURANÇA
​ESTA FERRAMENTA PODE SER PERIGOSA SE UTILIZADA INCORRETAMENTE. PROCEDA COM CAUTELA. 
Devido à arquitetura do Horizon OS, o overclock da memória RAM pode resultar em corrupção da NAND ou do cartão SD.
 Certifique-se de realizar um backup completo da NAND, PROINFO, EMUMMC e do cartão SD antes de prosseguir.

​Sobre o Projeto
​O Horizon OC é uma ferramenta de overclock de código aberto desenvolvida para consoles Nintendo Switch que operam sob o firmware customizado (CFW) Atmosphere. A aplicação viabiliza o ajuste avançado de CPU, GPU e RAM por meio de ferramentas de configuração intuitivas.

​Frequências Padrão (Clocks)
*​CPU(: Até 1963 MHz (Mariko) / 1785 MHz (Erista)
*​GPU*: Até 1075 MHz (Mariko) / 921 MHz (Erista)
*​RAM*: Até 1866/2133 MHz (Mariko) / 1600 MHz (Erista)

​Recursos Adicionais
​Suporte para Sobretensão e Subtensão (Over/Undervolting)
​Configurador integrado ao sistema
​Compatibilidade ampla com a maioria dos homebrews

​Recomenda-se a leitura prévia do guia técnico antes de prosseguir. Isto permitirá obter um ganho de desempenho expressivo em relação às configurações padrão, frequentemente reduzindo o consumo energético e a dissipação térmica.

​Procedimento de Instalação.

​Certifique-se de que o sistema possui as versões mais recentes dos seguintes componentes:


​Atmosphere
​Ultrahand Overlay
​Instruções de Instalação:

​Baixe e extraia o pacote Horizon OC Package diretamente na raiz do seu cartão SD.
​Caso utilize o gerenciador de boot Hekate, edite o arquivo hekate_ipl.ini para incluir as seguintes linhas:
comando para coloca no ipl do seu pacote
()*

kip1=atmosphere/kips/hoc.kip
secmon=atmosphere/exosphere.bin

*()



(Nenhuma alteração será necessária caso a inicialização seja realizada via fusee).

​Metodologia de Configuração

​Acesse o menu de sobreposição (Horizon OC Overlay).
​Abra o menu de configurações do sistema.
​Ajuste os parâmetros de overclock conforme desejado.

​Selecione a opção "Save KIP Settings" para aplicar e consolidar permanentemente a configuração.

​Compilação a partir do Código-Fonte
​Para instruções detalhadas de compilação, consulte o arquivo COMPILATION.md.

​Tabelas de Frequências (Clocks)

​Frequências de Memória *RAM* (MHz)

​3200 \rightarrow Limite máximo em hardware Mariko, padrão JEDEC.

​3166
​3133
​3100
​3066
​3033
​3000
​2966
​2933 \rightarrow Padrão JEDEC.
​2900
​2866
​2833
​2800
​2766
​2733
​2700
​2666 \rightarrow Padrão JEDEC.
​2633
​2600
​2566
​2533
​2500
​2466
​2433
​2400 \rightarrow Limite máximo em Erista, padrão JEDEC. (Estágio de nível máximo de overclock em Erista; dificilmente se conseguirá atingir esta frequência).

​2366
​2333
​2300
​2266
​2233
​2200
​2166
​2133 \rightarrow Limite máximo padrão Mariko JEDEC (Módulos de 4266 MT/s). (Modo recomendado caso queira utilizar overclock alto em hardware Mariko com possibilidade de expansão; esta frequência opera com estabilidade).

​2100
​2066
​2033
​2000
​1996 \rightarrow Padrão JEDEC.
​1966
​1933
​1900
​1866 \rightarrow Limite máximo comum para Erista. (Execute frequências superiores apenas para fins de teste; não recomendado para uso contínuo).

​1833
​1800
​1766
​1733
​1700
​1666
​1633
​1600 \rightarrow Modo oficial ancorado (Docked), modo Boost, limite máximo JEDEC para Erista (Módulos de 3200 MT/s), padrão JEDEC.

​1331 \rightarrow Modo oficial portátil (Handheld), padrão JEDEC.

​1065 Não é recomendável testar frequências de RAM inferiores a 1331 MHz em nenhuma revisão do console.


​800
​665
​Frequências de *CPU* (MHz)
​2703 \rightarrow Limite absoluto para hardware Mariko. Operação perigosa.


​2601 \rightarrow Operação insegura.

​2499
​2397
​2295
​2193
​2091 Limite máximo para hardware Erista. Evite utilizar em regime de overclock prolongado.


​1963 \rightarrow Frequência máxima para Mariko sem necessidade de Undervolting (UV).

​1887

​1785 \rightarrow Limite máximo padrão do módulo sys-clk para Erista.


​1683
​1581
​1428
​1326

​1224 \rightarrow Overclock de ambiente de desenvolvimento (sdev oc).

​1122

​1020 \rightarrow Perfil oficial para modos Ancorado (Docked) e Portátil (Handheld).


​918 Determinados títulos de software podem apresentar melhor otimização nesta frequência.

​816
​714

​612 \rightarrow Modo de suspensão / ociosidade (Sleep Mode). (Caso deseje utilizar o perfil mínimo na interface inicial e o escalonamento máximo permitido, não configure valores inferiores a este).


​Frequências de *GPU* (MHz)


​1536 \rightarrow Limite absoluto de frequência em Mariko. Operação altamente perigosa.

​1459
​1382
​1305


​1267 \rightarrow Especificação nominal do processador NVIDIA T214 (Mariko).


​1228 \rightarrow Frequência segura para Mariko sob perfil de alta subtensão (High UV).

​1152 \rightarrow Frequência máxima para Mariko sob perfil de otimização estendida (hiOpt-15mV).


​1075 \rightarrow Frequência máxima para Mariko sob perfil de otimização padrão (hiOpt). Limite absoluto de frequência para Erista. Operação altamente perigosa.


​998 \rightarrow Especificação nominal do processador NVIDIA T210 (Erista). (Evite a utilização, especialmente em modo portátil).


​960 (Exclusivo Erista) \rightarrow Frequência máxima segura para Erista sob perfis high uv / hiOpt-15mV. (Recomendado como limite máximo para testes em Erista no modo Ancorado/Dock).


​921 \rightarrow Frequência máxima para Erista sem necessidade de Undervolting (UV). (O perfil de alimentação por bateria suporta esta frequência nativamente, contudo, valores acima de 768 MHz devem ser restritos a cenários de estrita necessidade, não sendo fundamentais para o uso cotidiano).


​844

​768 \rightarrow Perfil oficial para modo Ancorado (Docked).


​691

​614 Limite máximo do sistema (sys-clk) para hardware Mariko em modo Portátil.


​537


​460 \rightarrow Limite máximo do sistema (sys-clk) para hardware Erista em modo Portátil.


​384 \rightarrow Perfil oficial para modo Portátil (Handheld).

​307 \rightarrow Perfil oficial para modo Portátil (Handheld).

​230 Modo de economia de energia. Não recomendado para execução de jogos devido à potencial perda de utilidade prática.


​153

​76 \rightarrow Modo de inicialização rápida / aceleração temporária (Boost Mode).


*​Notas Técnicas Adicionais*
​Na arquitetura Erista, a CPU operando em modo portátil possui um teto restritivo de 1581 MHz.
​O overclock de GPU em hardware Erista é limitado a 460 MHz quando em modo portátil.

​Na arquitetura Mariko, o limite operacional com o perfil hiOpt é de 614 MHz; com o perfil hiOpt-15mV eleva-se para 691 MHz e, sob o perfil High UV, atinge 768 MHz.


​GPU de Erista:
 (Há a possibilidade técnica de aplicar 768 MHz no modo portátil em Erista, contudo, solicita-se não exceder este patamar em modo portátil). Ocorrências de erros de gerenciamento de bateria e estresse severo de hardware são comuns caso o limite de 768 MHz seja ultrapassado no ecossistema Erista modo portatil


​Créditos e Agradecimentos
​Lightos's Cat – Desenvolvimento auxiliar (Cat)

​Souldbminer – Desenvolvimento dos módulos hoc-clk e do inicializador (loader)

​Lightos – Desenvolvimento de patches de inicialização, engenharia do hoc-clk e elaboração de guias técnicos

​TDRR – Design de identidade visual (Logotipo HOC)

​tetetete-ctrl – Desenvolvimento e design de interface web

​SciresM – Desenvolvimento do Firmware Customizado Atmosphere

​CTCaer – Desenvolvimento do ecossistema L4T, Hekate e calibração precisa de temporização de RAM (RAM timings)

​KazushiMe – Desenvolvimento do ecossistema Switch OC Suite

​Hanai3bi (Meha) – Desenvolvimento do Switch OC Suite, EOS e engenharia do sys-clk-eos

​NaGaa95 – Engenharia do Kernel L4T-OC e ramificação (fork) do módulo Status Monitor

​B3711 (halop) – Desenvolvimento do ecossistema EOS e contribuições gerais de código

​Equipe sys-clk (m4xw, p-sam, natinusala) – Desenvolvimento da suíte de controle sys-clk

​Dominatorul – Desenvolvimento de drivers
 Soctherm, elaboração de guias e consultoria técnica geral

​ppkantorski – Engenharia das ramificações (forks) do Ultrahand sys-clk e do Status Monitor

​MasaGratoR e ZachyCatGames – Consultoria e suporte técnico geral

​MasaGratoR – Desenvolvimento do Status
Monitor e implementação do driver Display Refresh Rate

​Dominatorul, Samybigio, Arcdelta, Miki, Happy, Winnerboi77, Blaise, Alvise, agjeococh, frost, letum00, e Xenshen – Controle de qualidade e testes laboratoriais de software

​Samybigio2011, Miki – Localização e tradução para o idioma italiano

​angelblaster – Localização e tradução para o idioma coreano

​q1332348216-glitch – Localização e tradução para o idioma chinês

​th3-ne0undr5c0r – Localização e tradução para o idioma francês

​Nvidia – Fornecimento do Manual Técnico de Referência do Tegra X1, desenvolvimento original do driver soctherm e arquitetura L4T
