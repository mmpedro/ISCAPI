# Integração de Serviços Comuns
A API de A Minha Rua é uma camada de integração, que disponibiliza um conjunto de operações com o objetivo de
 agilizar todos os processos de integração de sistemas externos à Plataforma de Serviços do [ePortugal](https://eportugal.gov.pt/servicos/comunicar-ocorrencias-no-espaco-publico-a-minha-rua).

- [Regressar ao ecrã inicial](../)

## Operações
As operações apresentadas representam as necessidades atuais e serão atualizadas conforme as necessidades.

## Registo de um problema
Registar uma ocorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|Form|Formulário eForms|1....1|

```markdown
<problem>
	<dateReported>?</dateReported>
	<title>?</title>
	<description>?</description>
	<personName>?</personName>
	<email>?</email>
	<phone>?</phone>
	<isPrivate>?</isPrivate>
	<host>?</host>
	<a>?
	</isActive>
	<status>?</status>
	<address>
		<postCode4></postCode4>
		<postCode3></postCode3>
		<postName></postName>
		<county></county>
		<district></district>
		<parish></parish>
	</address>
	<otherCategory>?</otherCategory>
	<comments>?</comments>
	<latitude>?</latitude>
	<addressType>?
	</typeAddress>
</problem>  
```
## Atualização de um problema
Atualizar uma ocorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|OperationCode|string|1....1|
|OperationVersion|string|1....1|
|Form|Formulário eForms|1....1|

```markdown
<update>
	<id></id>
	<changedate></changedate>
	<status>?</status>
	<comments></comments>
</update>  

```
## Obter ocorrências
Obter ocorrências

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|distrinc|string|1....1|
|county|string|1....1|
||parish|string||1....1|

```markdown
<search>
	<district></district>
	<county></county>
	<parish></parish>
	<status></status>
	<dateReportedStart></dateReportedStart>
	<dateSolvedEnd></dateSolvedEnd>
</search>  
```

## Obter imagem de uma oorrência

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|problemID|string|1....1|

```markdown
<getImage>
	<problemID></problemID>
</getImage> 
```
## Obter feedbkack

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|problemID|string|1....1|

```markdown
<getFeedback>
	<problemID></problemID>
</getFeedback> 
```


