# W-Analysis
Autores: [Andrés Felipe Duque Bran](afduquebr@unal.edu.co) \\
       [Nicolás Alejandro Ávila Pérez](navilap@unal.edu.co)

***
## Descripción
Este repositorio contiene el análisis del decaimiento bosón W con una luminosidad de 1 fb^-1 y energía del centro de masa de 8 TeV, tomando datos de 
formación académica encontrados en el [ATLAS Open Data Website](http://opendata.atlas.cern/extendedanalysis/datasets.php).

El bosón W tiene dos mecanismos de decaimiento en los cuales se encuentra un leptón como producto final:

  * W+ --> l+ v 
  * W- --> l- vbar
  
Uno de estos ejemplos se puede apreciar en la imagen siguiente, donde un bosón W- decae en un electrón e- y un anti neutrino.

![W- Boson Decay](images/W-boson_Decay.svg.png "W- Boson Decay")

De acuerdo con lo anterior, para el análisis se espera la obtención de un único leptón, y ningún jet. Asimismo, de acuerdo con el mecanismo expuesto, se espera 
la presencia de un neutrino, por lo cual este deberá verse reflejado en forma de energía transversa pérdida.

Por otro lado, el análisis de este decaimiento a partir de los datos del *ATLAS Open Data* cuenta con un ruido de fondo ocasionado por otros mecanismos 
que producen leptones.

  * ttbar production: Pueden generarse leptones cuando decae el bosón W generado.
  * Single Top Quark: Pueden generarse leptones cuando decae el bosón W generado.
  * Z Decay: El bosón Z es un proceso dileptónico.
  * Drell-Yan Process: Puede generar un bosón Z que decae en dos leptones de carga opuesta.
  * Diboson Production: Este proceso puede generar al menos un leptón sin importar el tipo de bosones que se escojan para el decaimiento.
  
Para este análisis se emplearon ambos datasets encontrados en el *ATLAS Open Data*

  * ```DataEgamma.root```
  * ```DataMuons.root```
  
***
## Análisis
Para el desarrollo del análisis del decaimiento del bosón W y la producción de los histogramas de las variables cinemáticas y selección de eventos se 
realizaron los siguientes cortes:

  * Canal de un solo leptón (muón o electrón).
  * Good Run List.
  * Buen vértice (Ntracks >4).
  * Buen leptón:
    * pT > 25 GeV.
    * Un solo leptón.
  * Energía transversa perdida mayor a 30 GeV.
  * Masa transversa del W mayor a 30 GeV.
  
A partir de esto se pudieron generar los histogramas. No obstante, debido a un error en el código no lograron obtenerse los diagramas para las siguientes 
variables:

  * Leading lepton eta.
  * Leading lepton phi.
  * Leading lepton etcone20.
  * Leading lepton ptcone30.
  
Por otro lado, se obtuvieron las entradas para cada uno de los procesos en los datos después de realizar los cortes necesarios para obtener un solo buen leptón.

  * W Decay: 5.8255 x 10^6 
  * ttbar Production: 38423
  * Single Top Quark: 10324
  * Z Decay: 2.1593 x 10^5
  * Drell-Yan Process: 12371
  * Diboson Production: 9068.6
  
Estos valores nos permiten apreciar que se realizó una buena selección sobre los datos y que la presencia de mecanismos de fondo se da debido a que existen 
otros procesos que logran generar un solo leptón.
