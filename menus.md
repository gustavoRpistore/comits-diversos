menus

id 

nome

&#x20;            ID1                                                                 ID2                                                      ID3

|eletrônicos<br />pcs<br />tus<br />ntebooks<br />videogames: Xbox, Playstation, Nintendo<br />|brinquedos<br /><br /><br /><br /><br /> |jogos<br /><br /><br /><br /><br />|
|-|-|-|





|ID<br />1<br />2<br />3<br />4 <br /><br /><br /><br /><br /><br /><br /><br />|NOME<br />ELETRONICOS<br />BRINQUEDOS<br />GAMES <br />PCS<br /><br /><br /><br /><br /><br /><br /><br /><br />|IDENENTIDADE PAI<br />NULL<br />NULL<br />NULL<br />1<br /> <br /><br /><br /><br /><br /><br /><br /><br />|
|-|-|-|





INTEGRIDADE 

* &#x20;conceito fundamental: correção, consistência e segurança de dados. estão associadas aos conceitos de chave de acesso. garantem o acesso individualizados a todas as ocorrências de uma tabela. garantem que os relacionamentos estejam validos e condizentes coma realidade 
* PK: chave primaria faz com que a tabela seja ordenada por ela automaticamente  e não permite duplicidade em seu valor mantem a unicidade dos dados. debe se elegar em um campo que não se repete 
* UK: chave única além da pk uma tabela pode possuir quantas uks forem necessárias, garante que não serão inseridos dados duplicados com colunas que não são pk
* SK: chave secundaria: chave auxiliar de acesso a uma tabela também possuem dados relacionados. utilizados em campos onde se efetua muitas pesquisas ou acessos noa precisam necessariamente ser uks
* FKS:  chaves estrangerias permite acesso e validação de outras tabelas. deve ser compatível em tipo e tamanho com sua pk correspondente na tabela de origem



Normalização 

organizar as tabelas de modo que suas estruturas sejam simples relacional e estável. o objetivo e evitar perdas e a repetição de informação apresentando e armazenando os dados adequadamente, melhora e estrutura dos dados e evita problemas de redundância e anomalias de atualização. e um processo sistemático de aplicação de regras que vão da primeira forma normal (fn) a quinta forma normal (fn) mas na grande maioria dos casos a aplicação da terceira forma normal já é suficiente 



primeira forma normal (fn) 

exige que uma tabela não tenha alinhamentos(atributos repetitivos). 

nivelamento

a pk (chave primaria) da tabela  e formada pelas pks de cada tabela adjacente 

caso existam atributos multivalorados  estes deem se tornar componentes da chave primaria, se existir alinhamento provavelmente este um fn não e o estado final do sheema 

uma tabela esta no fn se nenhum dos atributos possuem domínio multivalorado, ou seja devemos eliminar itens repetitivos

ex:



|nota fiscal                              <- versão normalizada <br />numero da nota<br />nome do cliente<br />nome vendedor<br />produto1<br />produto2<br />produto N<br />|primeira fn:<br />numero da nota<br />nome cliente<br />nome vendedor<br />item nota<br />chave estrangeira<br />numero da nota<br />código do produto<br />descrição do produto<br />valor|
|-|-|









2fn 

exige o entendimento do conceito de df dependência funcional, existe df em uma tabela que sempre tem um conjunto de um ou mais atributos determinando um valor de outro conjunto de um ou mais atributos

e possível perceber isto analisando dados de arquivos e relatórios de uma organização. 

uma tabela esta na segunda forma normal se e somente se estiver na primeira forma normal e todo atributo não chave depende funcionalmente de toda a chave primaria e não apenas de parte dela. devem existir dependência funcional da  chave primaria pk por completo. cada atributo não chave deve ser analisado e se identificado df de parte da pk 

gera-se uma tabela que tenha o atributo não chave e parte da chave primaria 

(que agora e uma pk completa)



a segunda forma normal fn2 

e o resultado da tabela de produtos onde o atributo determinante mais os outros que dependem apenas dele no caso nome foram movidos de nota e depois de item nota para produto 

compondo a pk composta em item nota







