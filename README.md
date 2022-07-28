<h3 align="center">
    <img alt="Logo" title="#logo" width="950px" src="https://github.com/kevinmiguel97/Criminality-Analysis-Mexico/blob/main/assets/map_municipios.png">
    <br>
</h3>

# Criminality-Analysis-Mexico for credit risk
- [Purpose](#purpose)
- [Tools applied](#tools)
- [Dataset description](#dataset)
- [Data cleaning](#cleaning)
- [Exploratory data analysis](#exploratory)

See the complete code [Notebook](Crime_analysis.ipynb)

<a id="purpose"></a>
## Purpose
Several factors must be considered when evaluating a loan granted by a financial instituions: liquidity, repayment capacity, leverage, financial ratios are examples of one of the most common ones. However, there some other more subtle attributes of loanees that might make a difference and that sometimes are easily overlooked. For Fintech companies that rely on more sophisticated ways to evaualte their applications, looking for these underlying factors takes a higher relevance. 

One factor that has been underexplored in recent years for this purpose is the level of criminality that exists in a specific region where a credit is been granted. 
The purpose of this project is to generate a database of the level of criminality that exists in México at a municipality or neighborhood level, depending on the available data. This database will be used for future projects of Data Science and Machine Learning models to predict in a more accurate way the probability of default. 

<a id="tools"></a>
## Tools applied
<div style="display: inline_block"><br>
  <img align="center" alt="Python" height="30" width="30" src="https://user-images.githubusercontent.com/77027441/171516140-314add44-18c2-4540-a58f-a6f461f9e80c.png">
  <img align="center" alt="Pandas" height="30" width="50" src="https://www.analyticslane.com/storage/2020/10/pandas.png">
  <img align="center" alt="Excel" height="30" width="40" src="https://1000marcas.net/wp-content/uploads/2020/12/Microsoft-Excel-Logo.png">
  <img align="center" alt="Folium" height="30" width="40" src="assets/folium_logo.jpg">  
  
 <a id="dataset"></a>
 ## Datasets descriptions
 For this project we worked with the following databases: 
 - ### [Crimes committed during 2021](data/delitos-datos-abiertos.csv) (Source: [Observatorio Nacional Ciudadano](https://delitosmexico.onc.org.mx/descargar))
     #### Variables: original name - code name (type):
        - inegi_entidad - id_entidad (int): Unique number for each of the 32 states in Mexico
        - entidad - entidad (string): Name of the state 
        - inegi_municipio - id_municipio (int): Unique number for each of the municipalities (example: 1001 -> Municipality 1 from state 1
                                                                                        1002 -> Municipality 2 from state 1) 
        - id_delito - id_delito: Unique number for each type of crime
        - delito - delito (string): Name of the crime
        - carpetas - carpetas (int): Number of open folders opened of the specific type of crime
        - tasa - tasa: Crimes for every 10,000 people
        
- ### [Population by municipality](data/poblaciones_2015.csv) (Source: [INAFED](https://www.gob.mx/inafed))
     #### Variables: original name - code name (type):
        - estado - entidad (string): Name of the state
        - municipio - municipio (string): Name of the municipality
        - cve_inegi - id_municipio: id_municipio (int): Unique number for each of the municipalities (example: 1001 -> Municipality 1 from state 1
                                                                                        1002 -> Municipality 2 from state 1) 
        - id_estado - id_entidad (int): Unique number for each of the 32 states in Mexico
        - hombres - hombres (int): Male population
        - mujeres - mujeres (int): Female population
        - total - total (int): Total population
        
- ### [Zip codes by neighborhood](data/codigos-postales-mexico.xlsx) (Source: [ExcelTotal](https://exceltotal.com/codigos-postales-de-mexico-en-excel/#google_vignette) based on Correos de México)
    ### Variables: original name - code name (type):
        - Código - cp (int): Zip code of the neighborhood
        - Asentamiento - Asentamineto (string): Name of neighborhood
        - Type - Type (string): Type of neighborhood
        - Municipality - municipio (string): Municipality Name
        - Ciudad - Ciudad (string): City Name
        - Estado - entidad (string): Name of the state
      
- ### [Coordenates of neighborhoods](data/coordenates_colonias.csv) (Source: [Eduardo Aranda](https://github.com/eduardoarandah/coordenadas-estados-municipios-localidades-de-mexico-json))
    ### Variables: original name - code name (type):
        - CVE_ENT - id_entidad (int): Unique number for each of the 32 states in Mexico
        - NOM_ENT - entidad (string): Name of the state
        - CVE_MUN - id_municipio (int): Unique number for each of the municipalities (example: 1 -> Municipality 1 without specifying state)
        - CVE_LOC - id_loc (int): Uniqe ID for each neighborhood 
        - NOM_LOC (string): Name of the neighborhood
        - LAT_DEC - lat (float): Lattitude
        - LON_DEC - lon (float): Longitude
        
 <a id="cleaning"></a>
 ## Data cleaning
 Because each dataset came from different sources, and the main goal of the project is to join them into a useful dataset containing the relevant variables, some data cleaning and specially data conciliation had to be made for all datasets used
 ### Conciliating data
        
        
                                                                                        
        
 
 
 
