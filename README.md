# Delays in domestic flights

In this project, we are interested in predicting and understanding delays in departure times for Brazilian airlines in domestic flights. There are three major companies, GOL, AZUL and TAM  which are denoted by the International Civil Aviation Organization (ICAO) abbreviation GLO, AZU, TAM. Here, we consider the data from 2018 - The National Civil Aviation Agency of Brazil (ANAC) has open data for all flights during that year. There are two different datasets, one that doesn't include the type of aircraft and another that does. Due to some inconsistencies, we will not merge them in one data frame, instead, we will use each dataset independently to see if aircraft type has any influence on the departure delays.

Note that departure delays can be separated into two independent types of delays: Propagated delays, which come from previous flights and intrinsic delays which are leg-dependent and has many components to them. The delay we experience in our everyday life is the sum of these two delays. Although in this project we regard only the total delay, a more complete dataset (with the whole Leg of each aircraft) can be used to distinguish the different delays and then use to predict the intrinsic delays.

## Instructions:

When running the code the first time, all data will be downloaded in the folders 'data' and 'data2'. In case the user might prefer to download, the folder 'data' uses flight data available at 'https://www.gov.br/anac/pt-br/assuntos/dados-e-estatisticas/percentuais-de-atrasos-e-cancelamentos-2/2018/' and national holidays available at 'https://www.anbima.com.br/feriados/fer_nacionais/2018.asp'. The folder 'data2' uses flight data available at 'https://siros.anac.gov.br/siros/registros/diversos/vra/2018/'. 

Adding the csv files in the folders will prompt the code to merge the flight data into a new file, in case a file is missing it will be downloaded automatically

## Data dictionary

Here we describe only the variables used during the analysis, for more information see the official documentation https://pergamum.anac.gov.br/arquivos/iac1504.pdf (in Portuguese).

- *ICAO_company*:
    ICAO abbreviation for the company name AZU (AZUL), GLO (GOL), TAM (LATAM)
- *Flight_type*:
    Flight type, 'N' is for domestic flight
- *ICAO_departure*: 
    ICAO abbreviation for the departure airport
- *ICAO_arrival*:
    ICAO abbreviation for the arrival airport
- *Expected_departure*:
    Expected departure time
- *Departure*:
    Real departure time
- *Expected_arrival*:
    Expected arrival time
- *Arrival*:
    Real arrival time
- *Flight_status*:
    can be either 'REALIZADO' (arrived) or 'CANCELADO' (cancelled) 
- *Aircraft*:
    ICAO code for aircraft type
- *Seats*:
    Number of seats in the aircraft
