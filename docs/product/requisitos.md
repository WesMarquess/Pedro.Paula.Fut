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

## Requisitos nao funcionais

| ID | Requisito | Criterio inicial |
| --- | --- | --- |
| RNF-01 | Responsividade | Jornadas principais utilizaveis em telas moveis e desktop. |
| RNF-02 | Acessibilidade | Contraste, foco visivel, labels e navegacao por teclado nas interfaces aplicaveis. |
| RNF-03 | Privacidade | Coletar apenas dados necessarios e restringir dados de contato por permissao. |
| RNF-04 | Seguranca | Autenticacao, autorizacao por perfil e validacao de entradas. |
| RNF-05 | Confiabilidade | Avaliacoes e dados moderados devem manter autor, data e vinculo com o role. |
| RNF-06 | Desempenho | Busca e listagem devem responder de forma adequada para uso interativo. |
| RNF-07 | Moderacao | Denuncias devem gerar estado rastreavel e permitir acao administrativa. |
| RNF-08 | Escalabilidade | O modelo deve permitir adicionar novas cidades, categorias e funcoes profissionais. |

## Regras de negocio iniciais

- Uma avaliacao deve estar vinculada a um role especifico.
- O sistema deve evitar mais de uma avaliacao ativa do mesmo usuario para a mesma participacao.
- A nota de um role deve ser calculada a partir das avaliacoes validas e publicadas.
- Conteudo denunciado pode ser ocultado enquanto aguarda moderacao.
- Uma oportunidade deve informar pelo menos funcao, data, local e forma de contato ou candidatura.
- Cada perfil deve ter um tipo de uso principal, mas pode acumular mais de um papel quando o produto permitir.
