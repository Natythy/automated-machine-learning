# automated-machine-learning

## Descrição do Desafio

O objetivo do desafio é explorar as capacidades de Machine Learning da plataforma Azure para desenvolver nossa primeira automação prática.

## Acesso a conta e criação do recurso de Machine Learning
1º Acesse sua conta no [Portal Azure](https://portal.azure.com);  

2º Ao selecionar + Create a resource, procure por Machine Learning e siga os próximos passo no vídeo:  

![screen-capture-ezgif com-effects](https://github.com/Natythy/automated-machine-learning/assets/88320974/8fb85d01-2966-4a4e-a266-29276b684cc4)

*Coloque um nome único de sua preferência*![Captura de tela 2024-03-20 061310](https://github.com/Natythy/automated-machine-learning/assets/88320974/940f9789-e41a-47dd-9d0b-324ec579ab36)  

*Após preencher as informações clique em "Review + Create"* ![Captura de tela 2024-03-20 061800](https://github.com/Natythy/automated-machine-learning/assets/88320974/b39ebd6c-1a10-40d5-9fe3-e12e2b3ac40b)

https://github.com/Natythy/automated-machine-learning/assets/88320974/59d37467-b990-4327-b53f-840140579695  

## Criação de uma Automated ML para o treino de modelo  


https://github.com/Natythy/automated-machine-learning/assets/88320974/84c239ea-ba14-47e7-889d-e0d5b6d53371

*Para criar uma Automated ML seguindo os seguintes passos:* 

BASIC SETTINGS:  

* **Job name:** mslearn-bike-automl  
* **New experiment name:** mslearn-bike-rental  
* **Description:** Automated machine learning for bike rental prediction  
* **Tags:** none  

TASK TYPE & DATA:  

* **Select task type:** Regression  
* **Select dataset:** Create a new dataset with the following settings:  
  * ***Data type:***
    * **Name:** bike-rentals
    * **Description:** Historic bike rental data
    * **Type:** Tabular
  * **Data source:**
    * Select From web files
 * **Web URL:**
    * **Web URL:** https://aka.ms/bike-rentals
    * **Skip data validation:** do not select
  * **Settings:**
    * **File format:** Delimited
    * **Delimiter:** Comma
    * **Encoding:** UTF-8
    * **Column headers:** Only first file has headers
    * **Skip rows:** None
    * **Dataset contains multi-line data:** do not select
  * **Schema:**
    * Include all columns other than Path
    * Review the automatically detected types
Selecione Create. Depois que o dataset for criado, selecione o bike-rentals dataset para continuar com o processo.

TASK SETTINGS:  

* **Task type:** Regression
* **Dataset:** bike-rentals
* **Target column:**  Rentals (integer)
* **Additional configuration settings:**
  * **Primary metric:** Normalized root mean squared error
  * **Explain best model:** Unselected
  * **Use all supported models:** Unselected.
  * **Allowed models:** Select only **RandomForest** and **LightGBM** 
* **Limits:** Expanda a sessão
  * **Max trials:** 3
  * **Max concurrent trials:** 3
  * **Max nodes:** 3
  * **Metric score threshold:** 0.085 
  * **Timeout:** 15
  * **Iteration timeout:** 15
  * **Enable early termination:** Selected
* **Validation and test:**
  * **Validation type:** Train-validation split
  * **Percentage of validation data:** 10
  * **Test dataset:** None  

COMPUTE:

* **Select compute type:** Serverless
* **Virtual machine type:** CPU
* **Virtual machine tier:** Dedicated
* **Virtual machine size:** Standard_DS3_V2*
* **Number of instances:** 1  


https://github.com/Natythy/automated-machine-learning/assets/88320974/4739a5b4-5b93-4c7e-a84c-654aa8cec434

## Modelo criado  


