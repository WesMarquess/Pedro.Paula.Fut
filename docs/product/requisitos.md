# Requisitos do produto

## Requisitos funcionais

| ID | Requisito | Prioridade |
| --- | --- | --- |
| RF-01 | Buscar roles por cidade, bairro, categoria ou palavra-chave. | Must |
| RF-02 | Filtrar roles por data, horario, preco, distancia e tipo de experiencia. | Must |
| RF-03 | Exibir detalhes do role: nome, descricao, categoria, local, horario, preco, contato e imagens quando disponiveis. | Must |
| RF-04 | Exibir nota media, quantidade de avaliacoes e comentarios de um role. | Must |
| RF-05 | Permitir que um usuario avalie um role apos informar que participou ou cumprir a regra de verificacao definida. | Must |
| RF-06 | Permitir denunciar uma avaliacao, role ou perfil. | Should |
| RF-07 | Permitir que a empresa cadastre e edite um role. | Should |
| RF-08 | Permitir que a empresa publique uma oportunidade de trabalho vinculada a um role. | Should |
| RF-09 | Permitir que o trabalhador informe funcoes, experiencia, localizacao e disponibilidade. | Should |
| RF-10 | Permitir que o trabalhador encontre oportunidades por funcao, data e localizacao. | Should |
| RF-11 | Permitir que o trabalhador manifeste interesse em uma oportunidade. | Should |
| RF-12 | Permitir que o administrador modere usuarios, roles, oportunidades e avaliacoes. | Must |

## Requisitos de qualidade do produto (ISO/IEC 25010)

Os requisitos abaixo aplicam o modelo de qualidade de produto da ISO/IEC 25010:2011. Cada item usa uma subcaracteristica do modelo, indica as personas afetadas e possui um criterio que pode ser validado em testes, inspecoes ou monitoramento. Os limites numericos sao metas iniciais do MVP e devem ser confirmados durante o piloto.

### Adequacao funcional

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-01 | Completude funcional | Turista, Rolezeiro, Trabalhador, Empresa, Admin | As jornadas principais devem cobrir busca e avaliacao de roles, cadastro de oportunidades, manifestacao de interesse e moderacao, conforme os RFs deste documento. |
| RNF-02 | Correcao funcional | Todas | Calculos de nota media, filtros, vinculos de avaliacao e estados de moderacao devem produzir resultados consistentes com os dados persistidos em testes de casos validos e invalidos. |
| RNF-03 | Pertinencia funcional | Turista, Rolezeiro, Trabalhador, Empresa | Cada resultado ou oportunidade exibido deve informar os dados necessarios para a decisao da persona: local, data, horario, categoria ou funcao, preco quando aplicavel e forma de contato ou candidatura. |

### Eficiencia de desempenho

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-04 | Comportamento em relacao ao tempo | Turista, Rolezeiro, Trabalhador | Em ambiente de referencia do MVP, busca e listagem devem responder em ate 2 segundos em pelo menos 95% das requisicoes e informar visualmente o carregamento quando exceder esse limite. |
| RNF-05 | Utilizacao de recursos | Todas | Consultas de busca, filtros e detalhes devem selecionar apenas os campos necessarios e nao degradar a navegacao por consumo excessivo de memoria ou rede em dispositivo movel de referencia. |
| RNF-06 | Capacidade | Empresa, Admin | O sistema deve suportar, no minimo, 100 usuarios concorrentes, 10.000 roles e 50.000 avaliacoes sem violar a meta de tempo do RNF-04. |

### Compatibilidade

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-07 | Coexistencia | Todas | A aplicacao deve funcionar sem bloquear outros aplicativos e sem exigir configuracao especial no dispositivo durante as jornadas moveis principais. |
| RNF-08 | Interoperabilidade | Turista, Empresa, Admin | Localizacao, imagens e dados de contato devem usar formatos e interfaces documentados, permitindo integracao com mapas e servicos autorizados sem expor dados alem da permissao concedida. |

### Usabilidade

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-09 | Reconhecimento de adequacao | Turista, Rolezeiro, Trabalhador | Uma pessoa deve identificar, na tela de resultados ou detalhes, se o role ou oportunidade combina com seus filtros sem precisar abrir mais de uma tela adicional por item. |
| RNF-10 | Aprendizibilidade | Todas | Um usuario novo deve concluir a busca de um role e abrir seus detalhes sem treinamento ou ajuda externa em teste de usabilidade. |
| RNF-11 | Operabilidade | Todas | A interface deve ser responsiva em mobile e desktop, ter navegacao por teclado, foco visivel, labels associados e mensagens de erro acionaveis. |
| RNF-12 | Protecao contra erro do usuario | Turista, Rolezeiro, Trabalhador, Empresa | Formularios devem validar campos obrigatorios antes do envio, preservar os dados digitados quando houver erro e pedir confirmacao antes de ocultar, excluir ou publicar conteudo. |
| RNF-13 | Acessibilidade | Todas | As jornadas principais devem atender WCAG 2.1 nivel AA como referencia, incluindo contraste, texto alternativo, sem dependencia exclusiva de cor e compatibilidade com leitor de tela quando aplicavel. |
| RNF-14 | Estetica da interface | Turista, Rolezeiro, Trabalhador, Empresa | Detalhes, precos, horarios, localizacao, notas e estados devem apresentar hierarquia visual consistente e linguagem compreensivel para cada persona. |
| RNF-15 | Acessibilidade percebida | Todas | O sistema deve exibir estados claros para carregamento, vazio, sucesso, erro e indisponibilidade de dados, sem deixar a persona sem orientacao sobre a proxima acao. |

### Confiabilidade

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-16 | Maturidade | Todas | Operacoes de cadastro, avaliacao, denuncia e candidatura devem ser cobertas por testes automatizados dos fluxos criticos antes de cada release do MVP. |
| RNF-17 | Disponibilidade | Turista, Rolezeiro, Trabalhador, Empresa | O servico deve atingir 99% de disponibilidade mensal no piloto, excluindo manutencoes comunicadas previamente. |
| RNF-18 | Tolerancia a falhas | Todas | Falhas de rede ou de servicos externos devem produzir mensagem compreensivel, permitir nova tentativa e nao criar avaliacao, candidatura ou denuncia duplicada. |
| RNF-19 | Recuperabilidade | Empresa, Admin | Deve existir copia de seguranca regular dos dados de roles, perfis, avaliacoes, oportunidades e moderacao, com restauracao testada no maximo a cada trimestre. |

### Seguranca

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-20 | Confidencialidade | Todas | Dados pessoais, contatos, candidaturas e historico de moderacao devem ser acessiveis somente ao titular ou a perfis autorizados, conforme a finalidade e permissao. |
| RNF-21 | Integridade | Todas | Avaliacoes devem manter autor, data e role; alteracoes em roles, oportunidades e moderacao devem registrar autor, data, operacao e valor alterado. |
| RNF-22 | Nao repudio | Admin, Empresa, Trabalhador | Acoes sensiveis, como publicar, denunciar, moderar e manifestar interesse, devem ser associadas a uma conta autenticada e ter registro consultavel quando aplicavel. |
| RNF-23 | Responsabilizacao | Admin | Denuncias e decisoes de moderacao devem possuir identificador, status, responsavel, motivo e historico de transicoes. |
| RNF-24 | Autenticidade | Todas | O sistema deve autenticar contas, aplicar autorizacao por perfil, validar entradas e proteger credenciais com praticas adequadas ao ambiente de execucao. |

### Manutenibilidade

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-25 | Modularidade | Todas | Busca, avaliacao, oportunidades, perfis e moderacao devem possuir responsabilidades separadas e interfaces internas documentadas, permitindo alterar um modulo sem quebrar os demais. |
| RNF-26 | Reusabilidade | Todas | Validacoes, controle de permissao, paginacao, tratamento de erros e componentes de interface recorrentes devem ser implementados de modo reutilizavel. |
| RNF-27 | Analisabilidade | Admin, Equipe de produto | Erros de producao e operacoes de moderacao devem gerar logs estruturados com identificador de correlacao, sem registrar dados pessoais desnecessarios. |
| RNF-28 | Modificabilidade | Empresa, Admin | Adicionar cidade, categoria, funcao profissional ou novo tipo de filtro deve exigir alteracoes localizadas, sem modificar a regra central de busca ou avaliacao. |
| RNF-29 | Testabilidade | Todas | Regras de nota, filtros, permissoes, denuncias e estados de oportunidade devem poder ser testadas sem depender de servicos externos. |

### Portabilidade

| ID | Subcaracteristica | Personas | Requisito e criterio de aceitacao |
| --- | --- | --- | --- |
| RNF-30 | Adaptabilidade | Turista, Rolezeiro, Trabalhador, Empresa | As jornadas principais devem se adaptar a telas de 360 px de largura ate desktop, sem perda de informacao ou acao essencial. |
| RNF-31 | Instalabilidade | Todas | O produto deve poder ser disponibilizado em ambiente novo seguindo um procedimento documentado, com configuracao separada de codigo, dados e segredos. |
| RNF-32 | Substituibilidade | Empresa, Admin | Integracoes externas, como mapas, imagens e notificacoes, devem ser acessadas por adaptadores, permitindo substitui-las sem alterar as regras de negocio. |

### Observacao sobre a edicao da norma

Este documento usa as oito caracteristicas da ISO/IEC 25010:2011, modelo adotado para a especificacao inicial. Em uma futura revisao baseada na edicao de 2023, os requisitos devem ser mapeados para as caracteristicas atualizadas, especialmente capacidade de interacao, flexibilidade e seguranca, incluindo protecao contra riscos de uso.

## Regras de negocio iniciais

- Uma avaliacao deve estar vinculada a um role especifico.
- O sistema deve evitar mais de uma avaliacao ativa do mesmo usuario para a mesma participacao.
- A nota de um role deve ser calculada a partir das avaliacoes validas e publicadas.
- Conteudo denunciado pode ser ocultado enquanto aguarda moderacao.
- Uma oportunidade deve informar pelo menos funcao, data, local e forma de contato ou candidatura.
- Cada perfil deve ter um tipo de uso principal, mas pode acumular mais de um papel quando o produto permitir.
