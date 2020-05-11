# Integração de Serviços Comuns
A API de A Minha Rua é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de
 agilizar todos os processos de integração de sistemas externos ao  [ePortugal](https://eportugal.gov.pt/servicos/comunicar-ocorrencias-no-espaco-publico-a-minha-rua).

- [Regressar ao ecrã inicial](../)

## Operações
As operações apresentadas representam as necessidades atuais e serão atualizadas conforme as necessidades.

## Registo de um problema
Registar uma ocorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|dateReported|string|1....1|
|title|string|1....1|
|description|string|1....1|
|description|string|1....1|

```markdown
<problem>
	<dateReported>?</dateReported>
	<title>?</title>
	<description>?</description>
	<citizen>
		<name></name>
		<email>?</email>
		<phone>?</phone>
	</citizen>
	<isPrivate>?</isPrivate>
	<system>?</system>
	<address>
		<postCode4></postCode4>
		<postCode3></postCode3>
		<postName></postName>
		<county></county>
		<district></district>
		<parish></parish>
		<addressType><addressType>
		<latitude></latitude>
		<Longitude></longitude>
	</address>
	<otherCategory>?</otherCategory>
	
	
	
</problem>  
```
## Atualização de um problema
Atualizar uma ocorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|idProblem|string|1....1|
|changeDate|string|1....1|
|status|string||1....1|
|comments|string||1....1|

```markdown
<update>
	<idProblem></idProblem>
	<changeDate></changeDate>
	<status>?</status>
	<comments></comments>
</update>  

```
## Obter ocorrências
Obter ocorrências

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|district|string|1....1|
|county|string|1....1|
|parish||string||1....1|

```markdown
<search>
	<district></district>
	<county></county>
	<parish></parish>
	<status></status>
	<dateReportedStart></dateReportedStart>
	<dateReportedEnd></dateReportedEnd>
	<dateSolvedStart></dateSolvedStart>
	<dateSolvedEnd></dateSolvedEnd>
</search>  
```

## Obter imagem de um problema
Obter a imagem associada ao problema reportado

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|problemID|string|1....1|

```markdown
<getImage>
	<problemID></problemID>
</getImage> 
```
## Obter feedbkack
Obter feedback de uma ocorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|problemID|string|1....1|

```markdown
<getFeedback>
	<problemID></problemID>
</getFeedback> 
```

## Enviar commentários
Colocar um comentário para o cidadão

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|problemID|string|1....1|

```markdown
<sendComments>
	<district></district>
	<county></county>
	<parish></parish>
	<problemID></problemID>
	<comments></comments>
</sendComments> 
```
## Categorias

| ID | Descrição|
|------------ | ------------|
|2|	Animais Abandonados|
|3|	Limpeza de Valetas, Bermas e Caminhos|
|4|	Conservação da Iluminação Pública|
|5|	Limpeza e Conservação de Espaços Públicos|
|6|	Saneamento, Ruturas de Águas ou Desvio de Tampas|
|7|	Sinalização de Trânsito|
|8|	Conservação de Parque Escolar|
|9|	Conservação das Ruas e Pavimento|
|10|Publicidade, Outdoors e Cartazes|
|11|Manutenção de Ciclovias|
|12|Recolha de Lixo|
|13|Manutenção, Rega e Limpeza de Jardins|
|14|Nomes ou Numeração de Ruas|
|15|Estacionamento de Veículos|
|16|Acessos para Cidadãos com Mobilidade Reduzida|
|17|Manutenção e Limpeza de Contentores e Ecopontos|
|19|Poluição Sonora|

## Estado

| ID | Descrição|
|------------ | ------------|
|0|Submetido|
|1|Em Análise|
|2|Resolvido|
|3|Não Aplicável|
|4|Reencaminhado|

