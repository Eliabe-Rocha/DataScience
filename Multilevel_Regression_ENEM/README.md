# Regressão Multinível com microdados do ENEM de 2020

[![NPM](https://img.shields.io/static/v1?label=author&message=Eliabe%20Rocha&color=red)](https://eliaberocha.netlify.app/)
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/Eliabe-Rocha/Multilevel_Regression_ENEM/blob/main/LICENSE)


# Sobre o projeto

<p>O projeto Regressão Multinível com microdados do ENEM de 2020 é um trabalho de conclusão de especialização (TCE) para obtenção do título de Especialista em Data Science e Analytics, pela Esalq/USP, defendido em 2022.</p>

O objetivo do estudo é compreender se variáveis como idade, raça, renda familiar e escolaridade parental geram impacto, e qual é esse impacto, sobre o desempenho dos participantes do Exame Nacional do Ensino Médio de 2020. 
O projeto foi dividido em três partes:
* Seleção e preparação dos dados para análise.
* Aplicação de estatística descritiva para análise dos grupos e compreensão dos comportamentos dos dados.
* Modelagem dos dados através do algorítimo de regressão multinível.

<p>Além disso, foi utilizado o framework de projetos CRISP-DM para a orientação das etapas de construção.</p>

# Ferramentas
Para aplicação das técnicas de estatística descritiva e modelagem dos dados foram utilizadas:
* Google Colab
* Google drive
* Linguagem de programação R e pacotes auxiliares como Tidyverse (tratamento dos dados) e nlme (para modelagem dos dados).

Os arquivos de texto e o código integral, bem com a base de dados utilizada podem ser acessados em:
[Repositório de Google Drive](https://drive.google.com/drive/folders/1L43ax_uqrvddX7_-XV3s539nBg_yW7Gb)



# Instalação

<p>Devido se tratar de um projeto de analytics, ou seja, não dispor de deploy, não há necessidade de qualquer instalação na máquina. Sendo necessário para sua reprodução somente a base de dados, presente no repositório ou baixado no próprio site da INEP, referente ao ano de 2020, e o script também presente no repositório.</p>
<p>O arquivo "Scrip_Final.ipynb" contém todas as bibliotecas para instalação e carregamento na sessão "Instalação e carregamento de pacotes".</p>


# Etapas

1. A primeira sessão do projeto, instalação e carregamento de pacotes, foca na instalação e carregamento das libraries, bem como conexão com o google drive para uso da base de dados. Foi acrescido um algoritmo para análise do p-value dos termos de erro no modelo multinível, desenvolvido pelo professor [Rafael de Freitas](https://www.linkedin.com/in/rafael-de-freitas-souza-a1465a1a8/).

2. Na segunda sessão, foi realizado o carregamento e a limpeza da base de dados. Foram aplicados filtros para escolha da amostra analisada no modelo, bem como acréscimo de variáveis de média geral e macrorregião de residência.

3. Na terceira sessão foi realizado o estudo dos grupos aos quais pertenciam os participantes do ENEM 2020. Técnicas de estatística descritiva foram utilizadas para entender a distribuição de participantes e desempenho por região, renda e nível de escolaridade familiar.

4. Na quarta parte foi realizado a modelagem dos dados em perspectiva de regressão linear e multinível.

5. Na última parte do projeto, sessão "Comparação e análise dos resultados", comparo o ajuste dos resíduos, bem como o loglik (métrica que indica acurácia do modelo) entre os modelos de regressão linear múltipla e o modelo multinível, visando entender qual faz mais sentido para análise.

## Importante

Alguns pontos importantes antes de executar os códigos:




<strike> 
* Por utilizar o colab e o armazenamento do Google Drive para o desenvolvimento do projeto, foi necessário realizar a conexão com o Google Drive utilizando as libraries httr, googledrive, httpuv e R.utils.
As células e  bibliotecas extras decorrem do fato do Google Colab não dispor de R Nativo, não sendo possível montar o armazenamento para acesso a base de dados, como em sua versão com python.
Caso o usuário deseje reproduzir o projeto localmente em sua máquina, as células 2 e 3 do script (referente a conexão e acesso Google Drive), as bibliotecas citadas acima, bem como a célula um da sessão "Carregamento e limpeza dos dados" podem ser descartadas.
</strike> 

* A base escolhida para o projeto, foi a base de microdados do ENEM de 2020. Seu download pode ser feito diretamente no site do [INEP](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem) ou diretamente na pasta dos arquivos do Drive. Anteriormente, o carregamento do arquivo era realizado através de conexão http com o google drive, porém devido a problemas de autenticações com o pacote e o google, optou-se por utilizar o carregamento direto na área de arquivos do google colab.
Vale ressaltar ainda que ao encerrar ou reiniciar a sessão, todos os arquivos na memória do colab são apagados, sendo necessários recarregá-los novamente.

* Em algumas etapas do código haverá a adiçã do código gc(), sua função é limpar o cache e resíduos da memória, funcional principalmente quando se está rodando localmente.

* Por se tratar de uma análise sem fins preditivos, não houve separação na base de dados entre treino e validação.
