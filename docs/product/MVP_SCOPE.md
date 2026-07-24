# Escopo do MVP — Predix Licita

## Regra central

O MVP não utilizará inteligência artificial.

Todas as pesquisas, classificações e alertas serão baseados em dados oficiais, filtros explícitos e regras determinísticas revisáveis.

## Regra de segurança

A pesquisa pública no PNCP pode ser desenvolvida antes da persistência privada. Entretanto, favoritos, notas, perfil empresarial, documentos e histórico de usuário somente poderão ser persistidos depois da implementação e validação de:

- autenticação;
- autorização;
- isolamento de dados;
- classificação de informações empresariais;
- retenção e exclusão;
- proteção de segredos;
- logs mínimos de auditoria.

## Funcionalidades incluídas

### 1. Consulta oficial ao PNCP

- integração somente leitura;
- coleta de oportunidades abertas;
- preservação do número de controle;
- URL oficial;
- data e hora da coleta;
- tratamento de falha e indisponibilidade.

### 2. Pesquisa por palavras

- busca no objeto e campos definidos;
- termos incluídos e excluídos;
- resultado paginado;
- indicação clara quando a pesquisa falhar ou não encontrar resultados.

### 3. Filtros

- UF;
- modalidade;
- faixa de valor, quando disponível;
- data de publicação;
- prazo final;
- situação aberta;
- execução remota ou local somente quando o dado estiver disponível.

### 4. Detalhes da oportunidade

- órgão;
- unidade;
- objeto;
- modalidade;
- local;
- datas;
- valor estimado;
- fonte;
- identificadores;
- campos ausentes destacados.

### 5. Controle de acesso e isolamento

Antes de funcionalidades privadas:

- autenticação;
- sessão segura;
- autorização;
- isolamento por usuário ou organização;
- tratamento de segredos;
- testes de acesso e negação;
- logs mínimos.

### 6. Oportunidades salvas

- salvar e remover favorito;
- estados: salva, em triagem, descartada e em preparação;
- notas internas;
- histórico mínimo de atualização;
- acesso restrito ao proprietário ou organização autorizada.

### 7. Acompanhamento de prazos

- dias restantes;
- ordenação por urgência;
- alertas internos configuráveis;
- indicação de prazo ausente ou encerrado.

### 8. Perfil empresarial

- identificação da empresa;
- porte;
- localização e áreas atendidas;
- CNAEs e objeto empresarial;
- capacidades declaradas;
- limite operacional definido pelo usuário;
- documentos e respectivas validades;
- experiências e atestados cadastrados manualmente;
- classificação de sensibilidade dos dados.

Nenhum dado empresarial será presumido.

### 9. Compatibilidade objetiva

O sistema poderá aplicar regras explícitas sobre dados disponíveis, como:

- prazo aberto;
- localização compatível;
- faixa de valor definida;
- termos relacionados às capacidades;
- documento cadastrado e válido;
- exigência conhecida versus dado empresarial disponível.

### 10. Bloqueadores e informações ausentes

Cada análise deve separar:

- compatibilidades confirmadas;
- possíveis bloqueadores;
- informações ausentes;
- itens que exigem leitura do edital;
- itens que exigem especialista humano.

### 11. Proveniência

Toda oportunidade deve mostrar:

- fonte oficial;
- URL;
- data e hora da coleta;
- versão ou atualização disponível;
- regra utilizada na classificação.

## Classificações permitidas no MVP

- `triagem favorável`;
- `triagem condicionada`;
- `bloqueio objetivo identificado`;
- `informação insuficiente`;
- `descartada pelo usuário`.

A expressão `compatibilidade confirmada` somente poderá ser usada quando todos os requisitos considerados estiverem documentados e verificados. O MVP não calcula probabilidade de vitória.

## Fora do MVP

- IA generativa;
- leitura automática integral de PDFs;
- extração automática de exigências;
- geração de proposta;
- envio ou participação automática;
- análise jurídica;
- previsão de resultado;
- múltiplas fontes além do PNCP;
- histórico de vencedores;
- análise de concorrência;
- integração com WhatsApp;
- cobrança e planos comerciais.

## Critério de conclusão do MVP

O MVP somente será considerado concluído quando:

- requisitos aprovados estiverem implementados;
- testes definidos estiverem verdes;
- fonte e coleta forem auditáveis;
- regras de classificação estiverem documentadas;
- falhas não forem apresentadas como ausência de oportunidades;
- controle de acesso e isolamento tiverem evidências;
- revisão independente emitir PASS;
- validação interna da Predix registrar utilidade real.