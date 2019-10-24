É uma linguagem para encontrar padrões de texto.
O regex precisa do alvo, o padrão e uma regex engine.

Alvo(target) ---- Pattern(regex) ----> Regex Engine(Uma linguagem de programação) => Resultado(Match)

Usamos expressões regulares para fazer validação de dados.
Extrair seções especificas de um arquivo de texto.
Validação de arquivos de texto e extração de dados para, por exemplo, gravar no banco de dados.
Substituindo os valores de um texto para limpar, reformatar ou alterar o conteúdo.
O regex faz uma análise de um determinado padrão de caracteres em uma string. Podemos usar este padrão para validade emails, telefones, CPF, CNPJ, etc. (Inputs no html já faz isso colocando uma classe de pattern="";

Meta caracteres( meta-char):
. o "ponto" que significa qualquer char
* o asterisco que serve para definir uma quantidade de chars, zero ou mais vezes
{ e } as chaves que servem para definir uma quantidade de caracteres específicas que é desejado encontrar
( e ) um meta carácter para definir um grupo

Classes de char [ e ]
[A-Z] de A a Z, sempre maiúscula
[a-z] de a a z, sempre minuscula
[A-Za-z] de A a Z ou a a z
[abc] somente a, b e c
[123] somente 1, 2 ou 3
\d para dígitos de 0 a 9. Forma reduzida de [0-9].
\s para espaços vazios(white spaces). Um atalho para, [ \t\r\n\f]. Sendo \t(tab), \r(carriage return), \n(newline) e \f(form feed).
\w para todos os charset existentes, não inclui caracteres especiais. Um atalho para [A-Za-z0-9_].

Quantifier
Os quantifiers são gananciosos por padrão e podemos utilizar um ? logo ele, deixando-o preguiçoso.
{n} exatamente n vezes
{n,} no minimo n vezes
{n,m} no minimo n e máximo m
? zero ou uma vez
* zero ou mais vezes
+ uma ou mais vezes
Ancoras
Existem ancoras predefinidas que selecionam uma posição dentro do alvo.
\b é uma ancora que seleciona um word boundary, isto é o inicio ou fim da palavra.
^ é uma ancora que seleciona o inicio da string alvo.
$ é uma ancora que seleciona o fim da string alvo.

Grupos
Podemos referenciar grupos dentro do regex. Usamos n.
Ex: Queremos achar uma tag de h1 ou h2, que tenha um ou mais caracteres, com caracteres especiais, e que termine com </ e o que foi escolhido no primeiro grupo. Terminando com >.
<(h1|h2).+?>([\w\sõãí.]+)<\/\1>
Non capturing groups
Para definir um grupo usamos as chaves, ( e ). Quando queremos que este grupo não seja marcado como grupo, usamos ?: para excluir eles do resultado. (?:)
