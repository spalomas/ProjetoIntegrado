## ***Disclaimer***
Este documento tem o objetivo de descrever o formato dos dados que compõe a base do Projeto, tal como as colunas que fazem parte de cada arquivo. 
Este arquivo foi elaborado através da análise dos arquivos CSV de amostra retirados do bucket S3 de *source* em conjunto com os PDFs descritivos das respectivas fontes: 
- Informe_Tecnico_SIASUS_2019_07.pdf - para os dados ambulatoriais;
- IT_SIHSUS_1603.pdf - para dados hospitalares.

Os arquivos citados acima estão disponibilizados nos Arquivos da Equipe, no *Microsoft Teams*.

A proposta deste documento é unificar em um único lugar todas as informações relacionadas aos dados *source*, para garantir total compreensão dos dados durante a tomada de decisão.
<br></br>

---

# Dados Ambulatoriais

### **Dicionário de dados - SIASUS**

**Formato do nome do arquivo:** PAUFaamm = Procedimento Ambulatorial + Unidade da Federação + ano + Mês
<br></br>
**ABMG1112.csv:** Arquivo APAC¹ de Cirurgia Bariátrica (MG) - pág 11 do PDF


**BIDF1201.csv:** Arquivo de Boletim de Produção Ambulatorial Individualizado (DF) - pág 17 do PDF


**BIPB2003.csv:** Arquivo de Boletim de Produção Ambulatorial Individualizado (PB) - pág 17 do PDF
<br></br>
## **Colunas** 

### **Para ABMG1112.csv**
**AP_MVM:** Data de Processamento / Movimento (AAAAMM)

**AP_CONDIC:** Sigla do Tipo de Gestão na qual o Estado ou Município está habilitado

**AP_GESTAO:** Código da Unidade de Federação + Código Município de Gestão ou UF0000 se a Unidade está sob Gestão Estadual

**AP_CODUNI:** Código do Estabelecimento no CNES (Cadastro Nacional de Estabelecimentos de Saúde)

**AP_AUTORIZ:** Número da APAC. Lei de formação: UFAATsssssssd, onde: UF – Unid. da Federação, AA – ano, T – tipo, sssssss – sequencial, d – dígito

**AP_CMP:** Data de Atendimento ao paciente / Competência (AAAAMM)

**AP_PRIPAL:** Procedimento Principal da APAC

**AP_VL_AP:** Valor Total da APAC Aprovado

**AP_UFMUN:** Código da Unidade da Federação + Código do Município do Estabelecimento

**AP_TPUPS:** Tipo de Estabelecimento

**AP_TIPPRE:** Tipo de Prestador

**AP_MN_IND:** Estabelecimento Mantido / Individual

**AP_CNPJCPF:** CNPJ do Estabelecimento executante

**AP_CNPJMNT:** CNPJ MANTENEDORA

**AP_CNSPCN:** Número do CNS (Cartão Nacional de Saúde) do paciente

**AP_COIDADE:** Código da Idade

**AP_NUIDADE:** Número da Idade

**AP_SEXO:** Sexo do paciente

**AP_RACACOR:** Raça/Cor do paciente: 01 - Branca, 02 - Preta, 03 - Parda, 04 - Amarela, 05 - Indígena, 99 - Sem informação

**AP_MUNPCN:** Código da UF + Código do Município de Residência do paciente

**AP_UFNACIO:** Nacionalidade do paciente

**AP_CEPPCN:** CEP do paciente

**AP_UFDIF:** Indica se a UF de residência do paciente é diferente da UF de localização do estabelecimento (N=não, S=sim)

**AP_MNDIF:** Indica se o município de residência do paciente é diferente do município de localização do estabelecimento (N=não, S=sim)

**AP_DTINIC:** Data de INÍCIO validade

**AP_DTFIM:** Data de FIM validade

**AP_TPATEN:** Tipo de Atendimento de APAC

**AP_TPAPAC:** Indica se a APAC é 1 - inicial, 2 - continuidade, 3 - única

**AP_MOTSAI:** Motivo de Saída e Permanência

**AP_OBITO:** Indicador de Óbito

**AP_ENCERR:** Indicador de Encerramento

**AP_PERMAN:** Indicador de Permanência

**AP_ALTA:** Indicador de Alta

**AP_TRANSF:** Indicador de Transferência

**AP_DTOCOR:** Data de Ocorrência que substitui a data de FIM de validade

**AP_CODEMI:** Código do Órgão emissor

**AP_CATEND:** Caráter do Atendimento

**AP_APACANT:** Número APAC Anterior

**AP_UNISOL:** Código CNES do Estabelecimento Solicitante

**AP_DTSOLIC:** Data da Solicitação

**AP_DTAUT:** Data da Autorização

**AP_CIDCAS:** CID Causas Associadas

**AP_CIDPRI:** CID Principal

**AP_CIDSEC:** CID Secundário

**AP_ETNIA:** Etnia do paciente

**AB_IMC:** IMC do paciente

**AB_PROCAIH:** Procedimento do AIH

**AB_DTCIRUR:** Data da Cirurgia

**AB_NUMAIH:** Número da AIH

**AB_PRCAIH2:** Procedimento do AIH

**AB_PRCAIH3:** Procedimento do AIH

**AB_NUMAIH2:** Número da AIH

**AB_DTCIRG2:** Data da Cirurgia

**AB_MESACOM:** Número em MESES de Acompanhamento

**AB_ANOACOM:** Ano de Acompanhamento

**AB_PONTBAR:** Pontuação de Baros

**AB_TABBARR:** Tabela de Baros

**AP_NATJUR:** Código da Natureza Jurídica

---

### **Para BIDF1201.csv e BIPB2003.csv**
**CODUNI:** Código do Estabelecimento no CNES (Cadastro Nacional de Estabelecimentos de Saúde)

**GESTAO:** Código da Unidade da Federação + Código do Município (IBGE) do Gestor, ou UF0000 se o estabelecimento estiver sob Gestão Estadual

**CONDIC:** Sigla do Tipo de Gestão no qual o Estado ou Município está habilitado

**UFMUN:** Código da Unidade da Federação + Código do Município onde está localizado o estabelecimento

**TPUPS:** Tipo de do Estabelecimento

**TIPPRE:** Tipo de Prestador

**MN_IND:** Estabelecimento Mantido / Individual

**CNPJCPF:** CNPJ do Estabelecimento executante

**CNPJMNT:** CNPJ da Mantenedora do estabelecimento ou zeros, caso não a tenha

**CNPJ_CC:** CNPJ do Órgão que recebeu pela produção por cessão de crédito ou zeros, caso não o tenha

**DT_PROCESS:** Ano e mês de Processamento da produção (AAAAMM)

**DT_ATEND:** Ano e mês do Atendimento (AAAAMM)

**PROC_ID:** Código do Procedimento Ambulatorial

**TPFIN:** Tipo de Financiamento da produção

**SUBFIN:** Subtipo de Financiamento da produção

**COMPLEX:** Complexidade do Procedimento

**AUTORIZ:** Número da APAC ou número de autorização do BPA²-I, conforme o caso. No BPA-I, não é obrigatório, portanto, não é criticado. Lei de formação: UFAATsssssssd, onde: UF – Unid. da Federação, AA – ano, T – tipo, sssssss – sequencial, d – dígito.

**CNSPROF:** Número do CNS (Cartão Nacional de Saúde) do profissional de saúde executante

**CBOPROF:** Código da Ocupação do profissional na Classificação Brasileira de Ocupações (Ministério do Trabalho)

**CIDPRI:** CID Principal

**CATEND:** Caráter de Atendimento

**CNS_PAC:** Número do CNS (Cartão Nacional de Saúde) do paciente

**DTNASC:** Data de nascimento do Paciente

**TPIDADEPAC:** Tipo da Idade do paciente em anos, meses ou dias. Calculado a partir da data de nascimento

**IDADEPAC:** Idade do Paciente

**SEXOPAC:** Sexo do paciente

**RACACOR:** Raça/Cor do paciente: 01 - Branca, 02 - Preta, 03 - Parda, 04 - Amarela, 05 - Indígena, 99 - Sem informação

**MUNPAC:** Código da Unidade da Federação + Código do Município de residência do paciente ou do estabelecimento, caso não se tenha a identificação do paciente, o que ocorre no (BPA)

**QT_APRES:** Quantidade Produzida (APRESENTADA)

**QT_APROV:** Quantidade Aprovada do procedimento

**VL_APRES:** Valor Produzido (APRESENTADO)

**VL_APROV:** Valor Aprovado do procedimento

**UFDIF:** Indica se a UF de residência do paciente é diferente da UF de localização do estabelecimento: 0 = mesma UF; 1 = UF diferente

**MNDIF:** Indica se o município de residência do paciente é diferente do município de localização do estabelecimento: 0 = mesmo município; 1 = município diferente

**ETNIA:** Conteúdo definido conforme Portaria SAS Nº 508, de 28 de Setembro de 2010. Anexo I. Preencher somente se o campo RACACOR for 05 - Indígena. A partir da competência Out/2010
<br></br>
**Lista de abreviaturas e Siglas**
> ¹*APAC*: ARQUIVOS DE AUTORIZAÇÕES DE PROCEDIMENTOS AMBULATORIAIS

> *Baros*: *Bariatric Analysis and Reporting Outcome System* - considerado o método mais eficaz e utilizado para a avaliação global do tratamento 
operatório da obesidade mórbida; porém, possui inúmeras críticas e precisa ser atualizado - ANÁLISE CRÍTICA DO MÉTODO BAROS: 
http://www.scielo.br/scielo.php?pid=S0102-67202015000600073&script=sci_arttext&tlng=pt

>*BPA²*: Boletim de produção ambulatorial. 
<br></br>

---

# Dados Hospitalares

### **Dicionário de dados - SIHSUS**

## **Colunas** 
### **Para CHBR1901** 
**CNES**: Código CNES do hospital;

**RAZAO**: Razão social do hospital;

**NOMEFANT**: Nome fantasia do hospital;

**CGC_HOSP**: CNPJ do estabelecimento;

**MUNIC_LOC**: Município - Códigos do IBGE;

**CNPJ_MANT**: CNPJ da mantenedora;

**CMPT**: ano+mês de processamento da AIH³ - (aaaamm).
<br></br>
**Lista de abreviaturas e Siglas**
> *AIH³*: Autorização de internação hospitalar.