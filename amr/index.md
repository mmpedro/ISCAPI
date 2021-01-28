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
	<person>
		<name>Jonh Doe</name>
		<email>john.doe@mail.com</email>
		<phone>?</phone>
	</person>
	<isPrivate>?</isPrivate>
	<channel>
		<webpage>www.eportugal.gov.pt</webpage>
	</channel>
	<location>
		<postCode4></postCode4>
		<postCode3></postCode3>
		<postName></postName>
		<county>01</county>
		<district>01</district>
		<parish>03</parish>
		<addressType><addressType>
		<latitude></latitude>
		<Longitude></longitude>
	</location>
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
|parish|string|1....1|

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

## Enviar comentários
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

## Obter categorias
Obter as categorias existentes para o reporte de problemas


## Obter distritos
Obter os distritos existentes de um distrito,


## Obter concelhos
Obter os concelhos existentes de um distrito , através do par DI do código dicofre.

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|DI|string|1....1|


```markdown
<county>
	<DI>10</DI>
</county>

```

## Obter Freguesia|s de um determinado concelho
Obter os distritos existentes de um distrito,

|Elemento| Tipo | Cardinalidade|
|------------ | ------------|
|DI|string|1....1|
|CO|string|1....1|


```markdown
  <parish>
			<DI>?</amr:DI>
            <CO>?</amr:CO>
  </parish>

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

## Estados

| ID | Descrição|
|------------ | ------------|
|0|Submetido|
|1|Em Análise|
|2|Resolvido|
|3|Não Aplicável|
|4|Reencaminhado|

## Tipo de Morada

| ID | Descrição|
|------------ | ------------|
|M|Municipio|
|F|Freguesia|


## Privado

| ID | Descrição|
|------------ | ------------|
|1|Sim|
|0|Não|

# Modelo de dados
![GSD1 phenotype]({{ BASE_PATH }}/ISCAPI/assets/images/amr.png)
