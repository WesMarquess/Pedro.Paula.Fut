# FIND MEU ROLE

Plataforma para descobrir experiencias na cidade, conectar empresas a profissionais freelancers e ajudar cada pessoa a encontrar o role que combina com seu momento e seus gostos.

## Visao

O FIND MEU ROLE aproxima tres necessidades que normalmente ficam separadas:

- Pessoas procurando algo interessante para fazer.
- Empresas procurando profissionais para operar seus eventos.
- Trabalhadores procurando oportunidades freelancers em eventos e estabelecimentos.

O produto combina descoberta local, recomendacoes por preferencia e confianca gerada por avaliacoes reais da comunidade.

## Problema

Encontrar um bom role ainda depende de informacao espalhada, indicacoes informais e pouca clareza sobre a experiencia esperada. Ao mesmo tempo, empresas tem dificuldade para encontrar profissionais disponiveis e trabalhadores precisam buscar oportunidades em varios canais.

## Proposta de valor

### Para quem quer sair

Encontrar festas, restaurantes, museus e outras experiencias com filtros relevantes, informacoes claras e avaliacoes de quem ja foi.

### Para quem trabalha

Encontrar servicos freelancers compativeis com sua funcao, localizacao, disponibilidade e experiencia.

### Para empresas

Publicar oportunidades e encontrar profissionais adequados para cada evento, com um historico de avaliacao que ajude na decisao.

## Escopo do MVP

O primeiro produto deve validar duas capacidades centrais:

1. **Encontrar roles:** listar e pesquisar roles por cidade, categoria, data, faixa de preco e preferencias.
2. **Avaliar roles:** permitir que usuarios avaliem experiencias frequentadas e consultem a nota e os comentarios de outros usuarios.

As conexoes entre empresas e trabalhadores entram como um segundo fluxo prioritario, com publicacao de vagas e demonstracao de interesse.

## Tipos de role

- Festa e balada
- Restaurante e gastronomia
- Museu e cultura
- Shows e musica ao vivo
- Feiras, eventos e experiencias locais

## Perfis atendidos

- **Admin:** garante qualidade, seguranca e organizacao da plataforma.
- **Turista:** quer conhecer a cidade com recomendacoes confiaveis.
- **Rolezeiro:** mora na cidade e busca experiencias alinhadas ao seu gosto.
- **Trabalhador:** procura servicos freelancers em eventos e estabelecimentos.
- **Empresa:** precisa divulgar roles e contratar profissionais.

Detalhes de cada perfil estao em [docs/personas/README.md](docs/personas/README.md).

## Requisitos funcionais iniciais

- RF-01: permitir encontrar roles por localizacao e categoria.
- RF-02: permitir filtrar roles por data, preco e preferencias.
- RF-03: exibir detalhes do role, incluindo local, horario, categoria e descricao.
- RF-04: permitir avaliar um role apos a participacao.
- RF-05: exibir nota media e avaliacoes de um role.
- RF-06: permitir que empresas publiquem oportunidades para seus eventos.
- RF-07: permitir que trabalhadores encontrem oportunidades por funcao e disponibilidade.
- RF-08: permitir que um usuario manifeste interesse em uma oportunidade.
- RF-09: permitir que administradores moderem roles, usuarios e avaliacoes.

## Requisitos de qualidade

Os requisitos nao funcionais foram reorganizados segundo as oito caracteristicas da ISO/IEC 25010:2011: adequacao funcional, eficiencia de desempenho, compatibilidade, usabilidade, confiabilidade, seguranca, manutenibilidade e portabilidade. Cada requisito possui criterio de aceitacao e rastreabilidade por persona em [docs/product/requisitos.md](docs/product/requisitos.md).

## Jornada principal do usuario

1. A pessoa informa cidade, data ou tipo de experiencia.
2. O sistema apresenta roles compativeis.
3. A pessoa compara detalhes, notas e comentarios.
4. A pessoa salva, compartilha ou acessa o role escolhido.
5. Depois da experiencia, avalia o role.

## Jornada de trabalho freelancer

1. O trabalhador cria seu perfil e informa funcoes, localizacao e disponibilidade.
2. Encontra oportunidades de DJ, barista, vendedor, seguranca, garcom e outras.
3. Consulta os detalhes do servico e manifesta interesse.
4. A empresa analisa os perfis e confirma a contratacao fora ou dentro da plataforma, conforme a evolucao do produto.

## Documentacao

- [Visao do produto](docs/product/visao-do-produto.md)
- [Requisitos funcionais e nao funcionais](docs/product/requisitos.md)
- [Indice de personas](docs/personas/README.md)

## Proximos passos sugeridos

1. Escolher uma cidade para o piloto.
2. Validar as jornadas com turistas, rolezeiros, trabalhadores e empresas.
3. Definir o modelo de dados de roles, avaliacoes, oportunidades e perfis.
4. Criar um prototipo da busca e da pagina de detalhes.
5. Implementar o MVP com dados reais de um grupo pequeno de parceiros.